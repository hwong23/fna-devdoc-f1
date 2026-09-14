---
name: Revision SDA por Fase
description: "Usar para evaluar documentos contra un subconjunto de plantillas SDA segun fase del proyecto, con decision formal de aprobacion >= 85%."
argument-hint: "Ruta carpeta raiz del caso y enfoque de revision"
agent: "SDA-agent"
---
Realiza una revision documental SDA por fase con el siguiente alcance:

- Carpeta raiz del caso: ${input:Ruta de carpeta raiz}
- Enfoque de riesgo: ${input:Riesgo principal (seguridad, integracion, transicion, gobierno)}

Estructura obligatoria esperada dentro de la carpeta raiz:
- documentos/
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- alcance/plantillas_incluidas.md
- alcance/plantillas_excluidas.md
- alcance/fase.md

Instrucciones de evaluacion:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la evaluacion.
- Carga plantillas validadoras solo desde plantillas/ y filtra por sufijo `_puntoycoma.csv`.
- Evalua solo el alcance declarado.
- No penalices plantillas fuera del alcance.
- Usa severidad Critico/Alto/Medio/Bajo.
- Calcula cumplimiento porcentual del alcance evaluado.
- Emite decision formal: Aprobado si cumplimiento >= 85%, No Aprobado en otro caso.

Devuelve salida con este formato:
1) Resumen Ejecutivo
2) Matriz de Cumplimiento por Plantilla
3) Hallazgos Priorizados
4) Trazabilidad y Coherencia
5) Checklist de Cierre
