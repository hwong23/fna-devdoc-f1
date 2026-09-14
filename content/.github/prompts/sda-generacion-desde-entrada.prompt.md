---
name: Generacion SDA desde Entrada
description: "Usar para analizar documentacion tecnica en carpeta de entrada y generar archivos documentales por plantilla SDA asociada usando solo *_puntoycoma.csv de plantillas/."
argument-hint: "Ruta carpeta raiz del caso y criterio de generacion"
agent: "SDA-agent"
---
Analiza una documentacion tecnica de entrada y genera la documentacion SDA pertinente por plantilla.

Entradas:
- Carpeta raiz del caso: ${input:Ruta de carpeta raiz}
- Objetivo del caso: ${input:Contexto del caso o iniciativa}
- Modo de generacion: ${input:Generacion-Individual o Generacion-Multiple}
- Plantilla objetivo: ${input:Nombre exacto de plantilla *_puntoycoma.csv o AUTO}
- Criterio de completitud: ${input:Estricta (solo evidencia explicita) o Asistida (permitir PENDIENTE_VALIDAR)}

Estructura obligatoria esperada dentro de la carpeta raiz:
- entrada/
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- salida/

Instrucciones de ejecucion:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la generacion.
- Carga plantillas validadoras solo desde plantillas/ y filtra por sufijo `_puntoycoma.csv`.
- Si el modo es Generacion-Individual, usa Plantilla objetivo. Si viene `AUTO`, pregunta al usuario cual plantilla desea y espera respuesta.
- Si el modo es Generacion-Multiple, analiza el contenido de entrada/ y determina que plantillas aplican.
- Si el modo es Generacion-Individual, genera en salida/ un solo archivo para la plantilla objetivo.
- Si el modo es Generacion-Multiple, genera en salida/ uno o varios archivos, uno por cada plantilla asociada al contenido.
- No inventes informacion. Si falta evidencia para campos, deja vacio o marca `PENDIENTE_VALIDAR`.
- Incluye trazabilidad evidencia->campo en el reporte final.

Salida requerida:
1) Resumen de Generacion (o Resumen de Generacion Individual)
2) Archivos Creados (o Archivo Creado en modo individual)
3) Mapeo Evidencia a Campos
4) Vacios y Validaciones Pendientes
