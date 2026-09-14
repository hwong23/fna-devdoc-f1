---
name: Generacion Individual por Plantilla SDA
description: "Usar para generar un unico documento SDA en salida/ a partir de entrada/, indicando explicitamente la plantilla objetivo *_puntoycoma.csv en plantillas/."
argument-hint: "Ruta carpeta raiz y plantilla objetivo"
agent: "SDA-agent"
---
Analiza documentacion tecnica en entrada/ y genera un unico archivo documental para la plantilla objetivo indicada.

Entradas:
- Carpeta raiz del caso: ${input:Ruta de carpeta raiz}
- Plantilla objetivo: ${input:Nombre exacto de plantilla *_puntoycoma.csv}
- Objetivo del caso: ${input:Contexto del caso o iniciativa}
- Criterio de completitud: ${input:Estricta o Asistida con PENDIENTE_VALIDAR}

Estructura obligatoria esperada dentro de la carpeta raiz:
- entrada/
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- salida/

Instrucciones de ejecucion:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la generacion.
- Verifica que la plantilla objetivo exista dentro de plantillas/ y termine en `_puntoycoma.csv`.
- Si la plantilla objetivo no existe o no cumple patron, pregunta una plantilla valida antes de continuar.
- Genera un solo archivo en salida/ asociado a la plantilla objetivo.
- No inventes informacion. Si falta evidencia para campos, deja vacio o marca `PENDIENTE_VALIDAR`.
- Incluye trazabilidad evidencia->campo en el reporte final.

Salida requerida:
1) Resumen de Generacion Individual
2) Archivo Creado (ruta, plantilla, estado)
3) Mapeo Evidencia a Campos
4) Vacios y Validaciones Pendientes
