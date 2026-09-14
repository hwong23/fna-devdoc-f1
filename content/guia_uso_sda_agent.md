# Guía de inicio y uso operativo de SDA-agent

## 1. Objetivo de esta guía
Esta guía explica como empezar a usar SDA-agent para revisar y generar documentación técnica de arquitectura bajo lineamientos SDA/TOGAF.

Incluye:
- Como preparar insumos.
- Como organizar carpetas según el tipo de revision.
- Como ejecutar los prompts disponibles.
- Como interpretar resultados y tomar decisiones.

---

## 2. Que hace SDA-agent
SDA-agent opera en tres modos:
- Revision: evalua documentación técnica contra plantillas validadoras del sistema documental.
- Generacion-Multiple: analiza documentación de entrada y crea archivos documentales por cada plantilla asociada.
- Generacion-Individual: analiza documentación de entrada y crea un unico archivo para una plantilla objetivo.

Reglas clave del agente:
- Solo usa plantillas en la carpeta `plantillas`.
- Solo considera archivos que terminan en `_puntoycoma.csv`.
- Ignora cualquier plantilla fuera de ese patron.
- No inicia evaluación si la estructura de entrada no cumple.

Escala de severidad de hallazgos:
- Critico
- Alto
- Medio
- Bajo

Decision formal:
- Aprobado si cumplimiento >= 85%
- No Aprobado si cumplimiento < 85%

---

## 3. Ubicación de componentes en el repositorio

### 3.1 Agente
- `.github/agents/SDA-agent.agent.md`

### 3.2 Prompts de ejecucion
- `.github/prompts/sda-revision-por-fase.prompt.md`
- `.github/prompts/sda-revision-integral.prompt.md`
- `.github/prompts/sda-trazabilidad-gap.prompt.md`
- `.github/prompts/sda-generacion-desde-entrada.prompt.md`
- `.github/prompts/sda-generacion-individual-plantilla.prompt.md`

---

## 4. Requisitos mínimos antes de ejecutar
1. Tener una carpeta raíz por caso de revision.
2. Incluir carpeta `plantillas` en esa raíz.
3. Verificar que las plantillas de validación sean solo `*_puntoycoma.csv`.
4. Incluir subcarpetas obligatorias según modalidad.
5. Si el modo es generación, incluir carpeta `entrada` y carpeta `salida`.
6. Si el modo es Generacion-Individual, indicar la plantilla objetivo por prompt o en `alcance/plantilla_objetivo.md`.
7. Definir el objetivo de la revision o de la generación.

---

## 5. Estructura de carpetas obligatoria por modalidad

## 5.1 Revision por fase
Estructura minima:

```text
<raiz-caso>/
  documentos/
  plantillas/
    catalogo_datos_plantilla_puntoycoma.csv
    catalogo_sistemas_plantilla_puntoycoma.csv
    catalogo_tecnologia_plantilla_puntoycoma.csv
    catalogo_requerimientos_plantilla_puntoycoma.csv
    matriz_integraciones_plantilla_puntoycoma.csv
    matriz_flujos_datos_plantilla_puntoycoma.csv
    matriz_transicion_arquitectura_plantilla_puntoycoma.csv
    matriz_brechas_soluciones_gobierno_plantilla_puntoycoma.csv
  alcance/
    fase.md
    plantillas_incluidas.md
    plantillas_excluidas.md
```

Uso recomendado:
- Cuando solo se audita un tramo del proyecto (ejemplo: certificación o producción).

## 5.2 Revision integral
Estructura minima:

```text
<raiz-caso>/
  plantillas/
    *_puntoycoma.csv
  catalogos/
  matrices/
  anexos/   (opcional)
```

Uso recomendado:
- Cuando se requiere una auditoria completa de cumplimiento SDA.

## 5.3 Trazabilidad y GAP
Estructura minima:

```text
<raiz-caso>/
  plantillas/
    *_puntoycoma.csv
  requerimientos/
  sistemas/
  datos/
  tecnologia/
  integraciones/
  transicion_gobierno/
```

Uso recomendado:
- Cuando se quiere encontrar quiebres de trazabilidad y brechas priorizadas.

## 5.4 Generación documental desde entrada técnica
Estructura minima:

```text
<raiz-caso>/
  entrada/
  plantillas/
    *_puntoycoma.csv
  salida/
```

Uso recomendado:
- Cuando existe uno o varios documentos técnicos fuente y se necesita construir la documentación SDA pertinente por plantilla.

## 5.5 Generación individual por plantilla
Estructura minima:

```text
<raiz-caso>/
  entrada/
  plantillas/
    *_puntoycoma.csv
  salida/
  alcance/               (opcional)
    plantilla_objetivo.md
```

Uso recomendado:
- Cuando se requiere construir solo un entregable documental para una plantilla especifica.

---

## 6. Como ejecutar el agente en VS Code

## 6.1 Opción recomendada: usar prompts
En el chat de VS Code:
1. Escribe `/`.
2. Selecciona uno de los prompts SDA.
3. Completa los campos solicitados (ruta raíz, contexto, enfoque).
4. Ejecuta.

## 6.2 Que prompt usar
- `Revision SDA por Fase`: para alcance parcial por etapa.
- `Revision SDA Integral`: para auditoria completa.
- `Trazabilidad y GAP SDA`: para enfoque en cadena y brechas.
- `Generacion SDA desde Entrada`: para generar en modo multiple o individual (si se indica plantilla objetivo).
- `Generacion Individual por Plantilla SDA`: para forzar la generacion de un unico archivo por plantilla objetivo.

Regla de seleccion de plantilla en generacion individual:
- Si el prompt trae plantilla objetivo valida, el agente genera directamente.
- Si el prompt trae `AUTO` o no indica plantilla, el agente pregunta cual plantilla usar antes de generar.

---

## 7. Como interpretar la salida
El formato de salida depende del modo ejecutado.

## 7.1 Salida en modo Revision
SDA-agent devuelve 5 bloques:

1. Resumen Ejecutivo
- Cumplimiento porcentual
- Decision formal (Aprobado/No Aprobado)
- Riesgo global
- Validacion de estructura de entrada
- Plantillas efectivamente usadas

2. Matriz de Cumplimiento por Plantilla
- Cobertura por plantilla (Completa/Parcial/Ausente)
- Evidencia
- Campos faltantes

3. Hallazgos Priorizados
- ID
- Severidad
- Evidencia
- Impacto
- Corrección recomendada

4. Trazabilidad y Coherencia
- Cadena minima:
  Requerimiento -> Sistema -> Dato -> Tecnologia -> Integracion/Flujo -> Transicion/Gobierno
- Huecos de trazabilidad

5. Checklist de Cierre
- Acciones en orden sugerido de ejecución

## 7.2 Salida en modo Generacion-Multiple
SDA-agent devuelve 4 bloques:

1. Resumen de Generación
- Carpeta de entrada analizada
- Plantillas candidatas detectadas
- Plantillas efectivamente generadas

2. Archivos Creados
- Ruta de cada archivo en `salida/`
- Plantilla origen asociada
- Estado (`Completo`, `Parcial`, `PENDIENTE_VALIDAR`)

3. Mapeo Evidencia a Campos
- Documento fuente
- Campo poblado
- Evidencia textual breve

4. Vacíos y Validaciones Pendientes
- Campos sin evidencia suficiente
- Datos pendientes de confirmación humana

## 7.3 Salida en modo Generacion-Individual
SDA-agent devuelve 4 bloques:

1. Resumen de Generacion Individual
- Plantilla objetivo seleccionada
- Carpeta de entrada analizada

2. Archivo Creado
- Ruta unica en `salida/`
- Plantilla origen
- Estado (`Completo`, `Parcial`, `PENDIENTE_VALIDAR`)

3. Mapeo Evidencia a Campos
- Documento fuente
- Campo poblado
- Evidencia textual breve

4. Vacíos y Validaciones Pendientes
- Campos sin evidencia suficiente
- Datos pendientes de confirmación humana

---

## 8. Criterio de aprobación y manejo de alcance parcial

## 8.1 Umbral de aprobación
- Si el cumplimiento es mayor o igual a 85%, el caso puede quedar Aprobado.
- Si es menor a 85%, queda No Aprobado.

## 8.2 Revisiones parciales por fase
- El agente evalúa solo lo declarado en alcance.
- No penaliza plantillas fuera del alcance.
- Debe quedar explicito que se evaluó y que se excluyo.

## 8.3 Criterio en modo Generacion-Multiple
- El agente no inventa datos.
- Si falta evidencia, deja el campo vacío o marca `PENDIENTE_VALIDAR`.
- Solo genera archivos para plantillas realmente asociadas al contenido de `entrada/`.

## 8.4 Criterio en modo Generacion-Individual
- El agente no inventa datos.
- Si falta evidencia, deja el campo vacio o marca `PENDIENTE_VALIDAR`.
- Si no hay plantilla objetivo valida, pregunta antes de generar.
- Genera un solo archivo en `salida/` para la plantilla objetivo.

---

## 9. Errores comunes y como evitarlos
1. Error: enviar archivos sueltos.
- Solución: moverlos a una carpeta raíz con estructura obligatoria.

2. Error: mezclar plantillas coma y puntoycoma.
- Solución: dejar en `plantillas` solo archivos `*_puntoycoma.csv`.

3. Error: omitir carpeta `plantillas`.
- Solución: crearla y cargar plantillas validadoras oficiales.

4. Error: no declarar alcance en revision por fase.
- Solución: completar `alcance/fase.md`, `plantillas_incluidas.md` y `plantillas_excluidas.md`.

5. Error: interpretar aprobado parcial como aprobado total.
- Solución: revisar el perímetro evaluado en el Resumen Ejecutivo.

6. Error: esperar que el agente genere todo sin carpeta de salida.
- Solución: crear `salida/` antes de ejecutar el prompt de generación.

7. Error: generar archivos para plantillas no relacionadas con el contenido.
- Solución: revisar el bloque "Plantillas candidatas detectadas" y mantener solo las asociadas a evidencia.

8. Error: ejecutar generacion individual sin plantilla objetivo.
- Solución: usar el prompt individual o indicar plantilla objetivo en el prompt general; si se usa `AUTO`, responder la pregunta del agente.

---

## 10. Flujo recomendado de adopcion en equipo
1. Definir una convención de nombre para carpetas de caso (ejemplo: `caso-YYYYMMDD-proveedor`).
2. Crear estructura base segun modalidad.
3. Copiar plantillas `*_puntoycoma.csv` en `plantillas`.
4. Cargar evidencias técnicas en subcarpetas correspondientes o en `entrada/` para generación.
5. Elegir modo de generacion (`Generacion-Multiple` o `Generacion-Individual`) cuando aplique.
6. Ejecutar el prompt SDA adecuado.
7. Si fue revision: corregir hallazgos Critico y Alto.
8. Si fue generación: validar campos `PENDIENTE_VALIDAR` con responsables funcionales/técnicos.
9. Reejecutar hasta alcanzar umbral (revision) o completar calidad documental (generación).
10. Presentar resultado en comité de arquitectura.

---

## 11. Plantilla rápida de inicio
Puedes usar este checklist antes de cada corrida:

```text
[ ] Tengo carpeta raiz del caso
[ ] Inclui carpeta plantillas
[ ] Solo tengo *_puntoycoma.csv en plantillas
[ ] Cree subcarpetas obligatorias segun modalidad
[ ] Defini alcance (si aplica) o criterio de generacion
[ ] Si es generacion individual, defini plantilla objetivo
[ ] Ejecute el prompt correcto
[ ] Revise decision formal y severidades (modo revision)
[ ] Revise archivos creados y PENDIENTE_VALIDAR (modo generacion)
[ ] Defini plan de cierre
```

---

## 12. Siguientes mejoras recomendadas
- Crear una carpeta modelo por cada modalidad para clonar rapidamente.
- Crear un prompt adicional de "precomite" con salida ejecutiva de una pagina.
- Definir SLA de remediación por severidad (Critico/Alto/Medio/Bajo).
