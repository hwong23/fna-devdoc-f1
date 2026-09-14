---
name: Revision SDA Integral
description: "Usar para auditoria completa contra las 8 plantillas del SDA y validacion integral de trazabilidad documental."
argument-hint: "Ruta carpeta raiz del caso y contexto del proveedor o proyecto"
agent: "SDA-agent"
---
Ejecuta una revision integral SDA sobre el material recibido.

Entradas:
- Carpeta raiz del caso: ${input:Ruta de carpeta raiz}
- Contexto de proveedor/proyecto: ${input:Contexto relevante}
- Nivel de profundidad: ${input:Basico, Intermedio, Exhaustivo}

Estructura obligatoria esperada dentro de la carpeta raiz:
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- catalogos/
- matrices/
- anexos/ (opcional)

Reglas:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la evaluacion.
- Carga plantillas validadoras solo desde plantillas/ y filtra por sufijo `_puntoycoma.csv`.
- Evalua las 8 plantillas SDA: catalogos, matrices, transicion y gobierno.
- Usa severidad Critico/Alto/Medio/Bajo.
- Exige evidencia textual por cada afirmacion de cumplimiento.
- Calcula cumplimiento total en porcentaje.
- Emite decision formal con umbral 85%.

Salida requerida:
1) Resumen Ejecutivo con decision formal
2) Matriz de Cumplimiento por Plantilla
3) Hallazgos Priorizados con impacto
4) Trazabilidad end-to-end y huecos
5) Plan de remediacion priorizado (30-60-90 dias)
