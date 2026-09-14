# Guia de inicio y uso operativo de SDA-agent

## 1. Objetivo de esta guía
Esta guia explica como empezar a usar SDA-agent para revisar documentos técnicos de arquitectura bajo lineamientos SDA/TOGAF.

Incluye:
- Como preparar insumos.
- Como organizar carpetas según el tipo de revision.
- Como ejecutar los prompts disponibles.
- Como interpretar resultados y tomar decisiones.

---

## 2. Que hace SDA-agent
SDA-agent revisa documentos técnicos contra plantillas validadoras del sistema documental.

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

---

## 4. Requisitos minimos antes de ejecutar
1. Tener una carpeta raiz por caso de revision.
2. Incluir carpeta `plantillas` en esa raiz.
3. Verificar que las plantillas de validacion sean solo `*_puntoycoma.csv`.
4. Incluir subcarpetas obligatorias segun modalidad.
5. Definir el objetivo de la revision (fase, integral o trazabilidad).

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
- Cuando solo se audita un tramo del proyecto (ejemplo: certificacion o produccion).

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

---

## 6. Como ejecutar el agente en VS Code

## 6.1 Opcion recomendada: usar prompts
En el chat de VS Code:
1. Escribe `/`.
2. Selecciona uno de los prompts SDA.
3. Completa los campos solicitados (ruta raiz, contexto, enfoque).
4. Ejecuta.

## 6.2 Que prompt usar
- `Revision SDA por Fase`: para alcance parcial por etapa.
- `Revision SDA Integral`: para auditoria completa.
- `Trazabilidad y GAP SDA`: para enfoque en cadena y brechas.

---

## 7. Como interpretar la salida
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
- Correccion recomendada

4. Trazabilidad y Coherencia
- Cadena minima:
  Requerimiento -> Sistema -> Dato -> Tecnologia -> Integracion/Flujo -> Transicion/Gobierno
- Huecos de trazabilidad

5. Checklist de Cierre
- Acciones en orden sugerido de ejecucion

---

## 8. Criterio de aprobacion y manejo de alcance parcial

## 8.1 Umbral de aprobacion
- Si el cumplimiento es mayor o igual a 85%, el caso puede quedar Aprobado.
- Si es menor a 85%, queda No Aprobado.

## 8.2 Revisiones parciales por fase
- El agente evalua solo lo declarado en alcance.
- No penaliza plantillas fuera del alcance.
- Debe quedar explicito que se evaluo y que se excluyo.

---

## 9. Errores comunes y como evitarlos
1. Error: enviar archivos sueltos.
- Solucion: moverlos a una carpeta raiz con estructura obligatoria.

2. Error: mezclar plantillas coma y puntoycoma.
- Solucion: dejar en `plantillas` solo archivos `*_puntoycoma.csv`.

3. Error: omitir carpeta `plantillas`.
- Solucion: crearla y cargar plantillas validadoras oficiales.

4. Error: no declarar alcance en revision por fase.
- Solucion: completar `alcance/fase.md`, `plantillas_incluidas.md` y `plantillas_excluidas.md`.

5. Error: interpretar aprobado parcial como aprobado total.
- Solucion: revisar el perimetro evaluado en el Resumen Ejecutivo.

---

## 10. Flujo recomendado de adopcion en equipo
1. Definir una convencion de nombre para carpetas de caso (ejemplo: `caso-YYYYMMDD-proveedor`).
2. Crear estructura base segun modalidad.
3. Copiar plantillas `*_puntoycoma.csv` en `plantillas`.
4. Cargar evidencias tecnicas en subcarpetas correspondientes.
5. Ejecutar prompt SDA.
6. Corregir hallazgos Critico y Alto.
7. Reejecutar hasta alcanzar umbral.
8. Presentar resultado en comite de arquitectura.

---

## 11. Plantilla rapida de inicio
Puedes usar este checklist antes de cada corrida:

```text
[ ] Tengo carpeta raiz del caso
[ ] Inclui carpeta plantillas
[ ] Solo tengo *_puntoycoma.csv en plantillas
[ ] Cree subcarpetas obligatorias segun modalidad
[ ] Defini alcance (si aplica)
[ ] Ejecute el prompt correcto
[ ] Revise decision formal y severidades
[ ] Defini plan de cierre
```

---

## 12. Siguientes mejoras recomendadas
- Crear una carpeta modelo por cada modalidad para clonar rapidamente.
- Crear un prompt adicional de "precomite" con salida ejecutiva de una pagina.
- Definir SLA de remediacion por severidad (Critico/Alto/Medio/Bajo).
