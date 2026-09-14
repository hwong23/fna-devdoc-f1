# Guia Metodologica del Sistema Documental de Arquitectura (SDA) Extendido
**Basado en TOGAF 9.2 (Architecture Content Framework & Repository) y ArchiMate 3.1**

---

## 1. Vision General del SDA Extendido

El **Sistema Documental de Arquitectura (SDA)** constituye la estructura central del **Repositorio de Arquitectura** de la organizacion. Su objetivo es gobernar, visibilizar y mantener la trazabilidad de los componentes de negocio, datos, aplicaciones e infraestructura, integrando tanto la vision logica (**Architecture Building Blocks - ABBs**) como la solucion fisica entregada por los proveedores tecnologicos (**Solution Building Blocks - SBBs**).

Para garantizar un gobierno integral de punta a punta, el SDA se organiza en tres capas de plantillas estandarizadoras en formato CSV:

1. **Catalogos de Inventario Base** (Poblacion de elementos unicos):
   - `catalogo_datos_plantilla.csv`: Entidades de datos logicas y componentes de almacenamiento fisicos.
   - `catalogo_sistemas_plantilla.csv`: Servicios de SI, componentes logicos y paquetes de software.
   - `catalogo_tecnologia_plantilla.csv`: Plataformas de software, servidores, redes y hardware.
   - `catalogo_requerimientos_plantilla.csv`: Requerimientos funcionales, no funcionales y restricciones.

2. **Matrices de Relacion e Integracion** (Interacciones y dinamica de datos):
   - `matriz_integraciones_plantilla.csv`: Mapeo de interfaces de comunicacion, protocolos (SOAP/REST/ETL) y endpoints salientes/entrantes.
   - `matriz_flujos_datos_plantilla.csv`: Trazabilidad del flujo de informacion, operaciones CRUD, mecanismos de carga e intercambios entre sistemas.

3. **Vistas de Cambio, Transicion y Gobierno** (Trazabilidad temporal y cumplimiento):
   - `matriz_transicion_arquitectura_plantilla.csv`: Evolucion incremental estado por estado (*Baseline*, *Transicion 1*, *Transicion 2*, *Target*) con acciones de cambio (*New*, *Retain*, *Replace*, *Retire*).
   - `matriz_brechas_soluciones_gobierno_plantilla.csv`: Trazabilidad entre brechas (*Gaps*), soluciones (*SBBs*), paquetes de trabajo (*Work Packages*) y comites de gobierno (*Architecture Board*).

---

## 2. Detalle de las Nuevas Plantillas del Repositorio

### A. Matriz de Integraciones (`matriz_integraciones_plantilla.csv`)
Esta matriz documenta el inventario de servicios y canales de comunicacion entre aplicaciones y componentes de terceros. Mapea la relacion entre los componentes logicos (ABBs) y los componentes de despliegue real (SBBs).

* **Campos Principales**:
  - `ID_Integracion`: Identificador unico (ej. `INT-001`).
  - `Nombre_Integracion`: Nombre funcional del servicio o interaccion.
  - `Sistema_Origen_ABB` / `Sistema_Origen_SBB`: Componente emisor (logico y fisico).
  - `Sistema_Destino_ABB` / `Sistema_Destino_SBB`: Componente receptor / backend (logico y fisico).
  - `Tipo_Integracion`: Protocolo o formato (SOAP, REST, ETL, Batch, Event-Driven/Platform Event).
  - `Patron_Sincronia`: Sincronico (Req-Reply), Asincronico, Publish-Subscribe.
  - `Endpoint_Origen_Exposicion`: URL o recurso expuesto por el origen.
  - `Endpoint_Destino_Consumo`: URL de consumo en el bus o backend (ej. endpoint ESB/COBIS).
  - `Mecanismo_Autenticacion`: OAuth 2.0, Basic Auth, Mutual TLS, Custom Header.
  - `Frecuencia_Volumen`: Estimacion de transacciones por dia / hora pico.
  - `Estado_CicloVida`: Baseline, Target, Transition, Phasing-Out.

---

### B. Matriz de Flujos de Datos (`matriz_flujos_datos_plantilla.csv`)
Inspirada en el *Data Dissemination Diagram* y la *Information Exchange Matrix* de TOGAF, especifica qué datos de negocio se mueven, con qué frecuencia, bajo qué operaciones y con qué nivel de seguridad.

* **Campos Principales**:
  - `ID_Flujo_Datos`: Identificador unico del flujo (ej. `DFLOW-001`).
  - `Nombre_Flujo`: Descripcion del proceso de transferencia.
  - `Entidad_Dato_Logica`: Entidad conceptual/logica (ej. *Cliente / Afiliado*, *Transaccion*).
  - `Componente_Dato_Fisico`: Tabla, vista, objeto CRM o BigObject donde se materializa.
  - `Rol_Dato`: Maestro (Familia A), Transaccional (Familia B), Log/Historico (Familia C).
  - `Sistema_Emisor_Origen` / `Sistema_Receptor_Destino`: Aplicaciones origen y destino.
  - `Operacion_CRUD`: Create, Read, Update, Delete.
  - `Tipo_Carga_Mecanismo`: Push por registro, Carga Masiva (DataLoader), Delta Batch.
  - `Transformacion_Homologacion`: Reglas de mapeo o tablas de homologacion aplicadas en el trayecto.
  - `Frecuencia_Ejecucion`: Tiempo real, Diario nocturno, Event-Driven.
  - `Sensibilidad_Seguridad`: Clasificacion de seguridad (PII, Confidencial, Publico).

---

### C. Matriz de Transicion de Arquitectura y Trazabilidad (`matriz_transicion_arquitectura_plantilla.csv`)
Basada en el *Transition Architecture State Evolution Table* y la tabla de *Increments* de TOGAF E/F, permite llevar el control estricto de la evolucion de los artefactos a lo largo de los *Plateaus* o estados temporales de transicion.

* **Campos Principales**:
  - `ID_Elemento`: Identificador del componente o servicio afectado.
  - `Nombre_Elemento`: Nombre del artefacto de arquitectura.
  - `Dominio_Arquitectura`: Negocio, Datos, Aplicacion, Tecnologia.
  - `Estado_Baseline_AsIs`: Estado en la operacion previa / legacy.
  - `Estado_Transicion_1_Cert`: Estado en el primer hito de entrega (ej. Certificacion/Sandbox).
  - `Estado_Transicion_2_Pilot`: Estado en el segundo hito (ej. Piloto/Go-Live Remediation).
  - `Estado_Target_ToBe`: Estado final deseado en produccion.
  - `Tipo_Accion_Cambio`: Taxonomia TOGAF/ArchiMate: *New* (Nuevo), *Retain* (Mantener), *Replace* (Reemplazar), *Retire* (Retirar), *Transition* (En transicion).
  - `Paquete_Trabajo_Proyecto`: Work Package o proyecto responsable del cambio.
  - `Justificacion_Brecha_Gap`: Brecha o necesidad tecnica/de negocio que motiva el cambio.
  - `Criterio_Salida_Gate`: Gate de calidad/KPI para aprobar la salida a la siguiente fase.
  - `Riesgo_Asociado`: Riesgo operativo durante la transicion.

---

### D. Matriz de Brechas, Soluciones y Gobierno (`matriz_brechas_soluciones_gobierno_plantilla.csv`)
Alineada con la *Consolidated Gaps, Solutions, and Dependencies Matrix* y el *Governance Log* de TOGAF, permite auditar que cada brecha identificada tenga una solucion tecnologica concreta (SBB), un ROI claro y la aprobacion del Comite de Arquitectura.

* **Campos Principales**:
  - `ID_Brecha_Gap`: Identificador de la brecha (ej. `GAP-DAT-01`).
  - `Dominio_Afectado`: Negocio, Datos, Aplicacion, Tecnologia, Gobierno.
  - `Descripcion_Brecha`: Deficiencia o diferencia entre el estado actual y el objetivo.
  - `Solucion_Propuesta_SBB`: Componente especifico o producto que resuelve la brecha.
  - `Paquete_Trabajo_Asociado`: Proyecto encargado de la implementacion.
  - `Dependencias_Tecnicas`: Requisitos previos o bloqueos con otros componentes.
  - `Prioridad_Negocio`: Alta, Media, Baja.
  - `Valor_Negocio_ROI`: Beneficio cuantificable o cualitativo.
  - `Mecanismo_Gobierno_Compliance`: Instancia de aprobacion (Architecture Board, Compliance Review, SLA Audit).
  - `Estado_Aprobacion`: Propuesto, En Revision, Aprobado, Exceptuado.

---

## 3. Flujo Operativo para Proveedores Tecnologicos y Gobierno

```
 [1. Asignacion]           [2. Diligenciamiento]         [3. Evaluacion Compliance]         [4. Carga Repositorio]
 Arquitectura entrega  -->  Proveedor completa CSVs  -->  Comite de Arquitectura       -->  Modelado EA / Archi
 plantillas al proveedor    (SBBs, Endpoints, Gaps)       evalua estandares y riesgos         Trazabilidad End-to-End
```

1. **Entrega de Plantillas**: El equipo de arquitectura entrega el kit de las 8 plantillas CSV al proveedor al inicio de la fase de disenio o construccion.
2. **Diligenciamiento por el Proveedor**: El proveedor completa la informacion tecnica detallando componentes fisicos, integraciones, endpoints reales, flujos de datos y la matriz de transicion de sus entregables.
3. **Validacion de Gobierno (Architecture Board)**: Se verifica la conformidad contra la Base de Estandares (*Standards Information Base - SIB*) de la empresa y se evaluan los criterios de salida (*Gates*) de la matriz de transicion.
4. **Carga en el Repositorio de Arquitectura**: Los archivos CSV planos se importan en la herramienta de modelado (ej. ArchiMate via CSV Importer / Enterprise Architect / iServer) para generar automaticamente los diagramas de interaccion, diagramas de despliegue y matrices de trazabilidad de cambios.

---

## 4. Resumen de Archivos del SDA en Studio

| Categoria | Nombre de Archivo CSV | Proposito en el Repositorio TOGAF |
| :--- | :--- | :--- |
| **Catalogos** | `catalogo_datos_plantilla.csv` | Entidades de datos logicas y componentes de almacenamiento. |
| **Catalogos** | `catalogo_sistemas_plantilla.csv` | Inventario de aplicaciones, servicios de SI y componentes. |
| **Catalogos** | `catalogo_tecnologia_plantilla.csv` | Infraestructura de hardware, software de sistema y redes. |
| **Catalogos** | `catalogo_requerimientos_plantilla.csv` | Requerimientos de arquitectura y restricciones tecnicas. |
| **Matrices** | `matriz_integraciones_plantilla.csv` | Interfaces, protocolos, endpoints y autenticacion. |
| **Matrices** | `matriz_flujos_datos_plantilla.csv` | Intercambio de datos, operaciones CRUD y mecanismos de carga. |
| **Transicion**| `matriz_transicion_arquitectura_plantilla.csv` | Evolucion temporal estado por estado (*Baseline* a *Target*). |
| **Gobierno**  | `matriz_brechas_soluciones_gobierno_plantilla.csv` | Trazabilidad de brechas (*Gaps*), soluciones (*SBBs*) y cumplimiento. |
