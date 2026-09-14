---
name: Trazabilidad y GAP SDA
description: "Usar para analisis focalizado de trazabilidad y brechas entre requerimientos, sistemas, datos, tecnologia, integraciones y gobierno."
argument-hint: "Ruta carpeta raiz del caso y dominio prioritario de analisis"
agent: "SDA-agent"
---
Analiza trazabilidad y brechas SDA con foco en cadena de valor arquitectonica.

Entradas:
- Carpeta raiz del caso: ${input:Ruta de carpeta raiz}
- Dominio prioritario: ${input:Negocio, Datos, Aplicacion, Tecnologia, Gobierno}
- Objetivo del analisis: ${input:Compliance, Riesgo, Preparacion de comite, Otro}

Estructura obligatoria esperada dentro de la carpeta raiz:
- plantillas/ (usar solo archivos `*_puntoycoma.csv`)
- requerimientos/
- sistemas/
- datos/
- tecnologia/
- integraciones/
- transicion_gobierno/

Procedimiento:
- Valida estructura de carpetas primero. Si no cumple, detalla faltantes y deten la evaluacion.
- Carga plantillas validadoras solo desde plantillas/ y filtra por sufijo `_puntoycoma.csv`.
- Reconstruye la cadena minima: Requerimiento -> Sistema -> Dato -> Tecnologia -> Integracion/Flujo -> Transicion/Gobierno.
- Identifica quiebres de trazabilidad y evidencia ausente.
- Clasifica severidad en Critico/Alto/Medio/Bajo.
- Estima cumplimiento porcentual del alcance analizado.
- Emite decision formal con umbral de 85%.

Entrega:
1) Mapa de trazabilidad consolidado
2) Lista de GAPs con causa e impacto
3) Riesgos de gobierno y conformidad
4) Acciones correctivas priorizadas
5) Decision formal de aprobacion
