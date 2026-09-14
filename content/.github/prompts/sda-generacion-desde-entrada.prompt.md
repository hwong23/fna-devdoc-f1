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
- Criterio de completitud: ${input:Estricta (solo evidencia explicita) o Asistida (permitir PENDIENTE_VALIDAR)}

Estructura obligatoria esperada dentro de la carpeta raiz:
- entrada/
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- salida/

Instrucciones de ejecucion:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la generacion.
- Carga plantillas validadoras solo desde plantillas/ y filtra por sufijo `_puntoycoma.csv`.
- Analiza el contenido de entrada/ y determina que plantillas aplican.
- Genera en salida/ uno o varios archivos, uno por cada plantilla asociada al contenido.
- No inventes informacion. Si falta evidencia para campos, deja vacio o marca `PENDIENTE_VALIDAR`.
- Incluye trazabilidad evidencia->campo en el reporte final.

Salida requerida:
1) Resumen de Generacion
2) Archivos Creados (ruta, plantilla, estado)
3) Mapeo Evidencia a Campos
4) Vacios y Validaciones Pendientes
