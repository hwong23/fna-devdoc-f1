# Guía Unificada del Sistema Documental de Arquitectura (SDA)
## Marco de trabajo basado en TOGAF ADM y ArchiMate 3.1

**Uso interno y para distribución a proveedores tecnológicos**

--- 

## Vision General del SDA

El **Sistema Documental de Arquitectura (SDA)** constituye la estructura central del 
**Repositorio de Arquitectura** de la organización. Su objetivo es gobernar, visibilizar y 
mantener la trazabilidad de los componentes de negocio, datos, aplicaciones e infraestructura, 
integrando tanto la vision lógica (**Architecture Building Blocks - ABBs**) como la solución física 
entregada por los proveedores tecnológicos (**Solution Building Blocks - SBB**).

Para garantizar un gobierno integral de punta a punta, el SDA se organiza en tres capas de plantillas 
estandarizadoras en formato CSV:

1. **Catalogos de Inventario Base** (Poblacion de elementos unicos):
   - `catalogo_datos_plantilla.csv`: Entidades de datos lógicas y componentes de almacenamiento físicos.
   - `catalogo_sistemas_plantilla.csv`: Servicios de SI, componentes lógicos y paquetes de software.
   - `catalogo_tecnologia_plantilla.csv`: Plataformas de software, servidores, redes y hardware.
   - `catalogo_requerimientos_plantilla.csv`: Requerimientos funcionales, no funcionales y restricciones.

2. **Matrices de Relación e Integracion** (Interacciones y dinámica de datos):
   - `matriz_integraciones_plantilla.csv`: Mapeo de interfaces de comunicación, protocolos (SOAP/REST/ETL) y endpoints salientes/entrantes.
   - `matriz_flujos_datos_plantilla.csv`: Trazabilidad del flujo de información, operaciones CRUD, mecanismos de carga e intercambios entre sistemas.

3. **Vistas de Cambio, Transicion y Gobierno** (Trazabilidad temporal y cumplimiento):
   - `matriz_transicion_arquitectura_plantilla.csv`: Evolución incremental estado por estado (*Baseline*, *Transicion 1*, *Transicion 2*, *Target*) con acciones de cambio (*New*, *Retain*, *Replace*, *Retire*).
   - `matriz_brechas_soluciones_gobierno_plantilla.csv`: Trazabilidad entre brechas (*Gaps*), soluciones (*SBB*), paquetes de trabajo (*Work Packages*) y comités de gobierno (*Architecture Board*).

---

## 1. Propósito del SDA

El Sistema Documental de Arquitectura (SDA) es la estructura central del repositorio de arquitectura de la organización. Su objetivo es gobernar, estandarizar y mantener la trazabilidad de los activos de negocio, datos, aplicaciones, infraestructura y requerimientos, integrando tanto la visión lógica de la organización como la solución física entregada por proveedores tecnológicos.

El SDA está alineado con:
- TOGAF 9.2, especialmente en su enfoque de Architecture Repository, Content Metamodel, Architecture Landscape y Governance.
- ArchiMate 3.1, como lenguaje para describir las relaciones entre elementos de negocio, aplicación, datos y tecnología.

El sistema busca facilitar:
- la estandarización documental de la arquitectura empresarial,
- la trazabilidad end-to-end de soluciones,
- la conformidad con estándares internos,
- la reducción de brechas entre el estado actual y el objetivo,
- y la alineación entre estrategia, operación y tecnología.

---

## 2. Fundamentos del repositorio de arquitectura

El SDA se organiza en torno a tres pilares del enfoque TOGAF:

### 2.1 Bloques de construcción: ABB vs. SBB

**Architecture Building Blocks (ABB)**
- Representan capacidades lógicas y abstractas.
- Son independientes de tecnología y proveedor.
- Definen qué debe existir en la arquitectura empresarial.
- Ejemplos: servicio de gestión de clientes, motor relacional de base de datos, servicio de autenticación.

**Solution Building Blocks (SBB)**
- Representan implementaciones concretas, productos, servicios o componentes físicos.
- Son específicos de proveedor, versión y despliegue.
- Responden a la pregunta: ¿cómo se implementa la capacidad en la solución real?
- Ejemplos: Salesforce Service Cloud, PostgreSQL en AWS, Microsoft Azure AD B2C.

La relación entre ambos es clave para la gobernanza: los ABB definen la necesidad y los SBB la materializan.

### 2.2 Repositorio de arquitectura

El Repositorio de Arquitectura de la empresa actúa como un archivo centralizado gobernado bajo las siguientes 
áreas (TOGAF):

1.  **Metamodelo de Arquitectura (Architecture Metamodel)**: El esquema maestro que define la taxonomía de los elementos lógicos y físicos y sus interrelaciones.
2.  **Panorama de Arquitectura (Architecture Landscape)**: El estado actual y objetivo de los activos (lógicos e implementados) de la empresa a niveles Estratégico, de Segmento y de Capacidad.
3.  **Base de Información de Estándares (SIB - Standards Information Base)**: Define las tecnologías aprobadas, estándares de la industria y la clasificación de ciclo de vida (estándar, provisorio, retirado, en obsolescencia) con las que las soluciones de los proveedores deben cumplir.
4.  **Biblioteca de Referencia (Reference Library)**: Contiene plantillas, directrices y patrones reutilizables.
5.  **Repositorio de Requerimientos (Requirements Repository)**: Centraliza los requerimientos de arquitectura, técnicos y no funcionales que guían los proyectos.
6.  **Panorama de Soluciones (Solutions Landscape)**: Registro de los SBB implementados y desplegados por los proveedores tecnológicos.
7.  **Bitácora de Gobierno (Governance Log)**: Registro de decisiones de arquitectura, evaluaciones de conformidad y aprobaciones de proyectos.

### 2.3 Metamodelo de contenido

El metamodelo de contenido organiza la arquitectura en dominios clave:
- negocio,
- datos,
- aplicaciones,
- tecnología,
- requerimientos,
- y gobierno.

Los archivos del SDA alimentan este metamodelo y permiten construir trazabilidad entre elementos lógicos, físicos y de transición.

Para alimentar este repositorio, los proveedores deben suministrar información estructurada 
en **4 Catálogos Individuales**. Cada plantilla CSV mapea directamente a entidades del metamodelo (TOGAF):

```
+---------------------------------------------------------------------------------+
|                                 SDA REPOSITORIO                                 |
|                                                                                 |
|  +--------------------+  +--------------------+  +---------------------------+  |
|  |  Catálogo de Datos |  |Catálogo de Sistemas|  |  Catálogo de Tecnología   |  |
|  | (Data Component &  |  |   & Componentes    |  |   (Infraestructura HW/SW  |  |
|  |    Data Entity)    |  | (Application Port.)|  |    Standards/Portfolio)   |  |
|  +--------------------+  +--------------------+  +---------------------------+  |
|            ^                       ^                           ^                |
|            |                       |                           |                |
|            +-----------------------+---------------------------+                |
|                                    | (Alineados a)                              |
|                         +-----------------------+                               |
|                         |      Catálogo de      |                               |
|                         |    Requerimientos     |                               |
|                         +-----------------------+                               |
+---------------------------------------------------------------------------------+
```

---

## 3. Estructura del SDA y tipos de archivos

El SDA se compone de tres grupos principales de artefactos:

### 3.1 Catálogos de inventario base
Estos archivos documentan los elementos principales del repositorio y forman la base de la solución.

- `catalogo_datos_plantilla.csv`
- `catalogo_sistemas_plantilla.csv`
- `catalogo_tecnologia_plantilla.csv`
- `catalogo_requerimientos_plantilla.csv`

### 3.2 Matrices de integración y trazabilidad
Estos artefactos capturan relaciones, flujos, dependencias y cambios entre elementos.

- `matriz_integraciones_plantilla.csv`
- `matriz_flujos_datos_plantilla.csv`
- `matriz_transicion_arquitectura_plantilla.csv`
- `matriz_brechas_soluciones_gobierno_plantilla.csv`

### 3.3 Finalidad operativa

La combinación de catálogos y matrices permite:
- identificar inventarios de datos, sistemas y tecnología,
- mapear interfaces y flujos de información,
- registrar evolución temporal de los activos,
- y asociar brechas con soluciones, dependencias y mecanismos de gobierno.

---

## 4. Catálogos del SDA

### 4.1 Plantilla 1: Catálogo de Datos (catalogo_datos_plantilla.csv)
**Objetivo**: Identificar los activos de información de la empresa, los componentes lógicos que los agrupan (para gobernanza y seguridad) y los repositorios físicos (bases de datos, esquemas) donde se almacenan físicamente.

*   **Entidades Metamodelo Soportadas**: *Data Entity, Logical Data Component, Physical Data Component*.
*   **Campos de la Plantilla**:
    1.  `ID_Elemento`: Identificador único según nomenclatura (ej. DAT-ABB-001, DAT-SBB-001).
    2.  `Tipo_Elemento`: Debe especificarse si es un componente de datos lógico (*Logical Data Component*), un componente físico o base de datos (*Physical Data Component*) o una entidad lógica de negocio (*Data Entity*).
    3.  `Nombre`: Nombre descriptivo legible (ej. Maestro de Clientes).
    4.  `Descripcion`: Propósito del almacenamiento o definición del dominio del dato.
    5.  `Clasificacion_ABB_SBB`: Indica si corresponde a la definición abstracta de datos (`ABB`) o al producto físico implementado (`SBB`).
    6.  `Modulo_LGC_Asociado ->`: Vínculo para asociar entidades a su componente lógico.
    7.  `Tecnologia_Almacenamiento`: Motor de base de datos o almacenamiento físico utilizado (solo para SBB).
    8.  `Clasificacion_Seguridad`: Nivel de sensibilidad del dato (*Público, Interno, Confidencial, Restringido*).
    9.  `Propietario_Datos`: Área del negocio dueña del dato.
    10. `Origen_Registro_Sistema ->`: Sistema de origen que se considera la "aplicación de registro" productora del dato.
    11. `Volumetria_Estimada`: Cantidad aproximada de registros.
    12. `Frecuencia_Actualizacion`: Tiempo de refresco (ej. Tiempo Real, Diario, Mensual).

**Uso**:
- definir qué datos existen,
- dónde se materializan,
- quién los administra,
- y qué nivel de sensibilidad tienen.

### 4.2 Plantilla 2: Catálogo de Sistemas y Componentes (catalogo_sistemas_plantilla.csv)
**Objetivo**: Mantener el inventario unificado de aplicaciones (*Application Portfolio*) y servicios de TI de la empresa. Permite identificar la obsolescencia tecnológica, el solapamiento funcional y definir el alcance de los proyectos de cambio.

*   **Entidades Metamodelo Soportadas**: *Information System Service, Logical Application Component, Physical Application Component*.
*   **Campos de la Plantilla**:
    1.  `ID_Componente`: Identificador único (ej. APP-ABB-001, APP-SBB-001).
    2.  `Tipo_Elemento`: Tipo de entidad (*Logical Application Component, Physical Application Component, Information System Service*).
    3.  `Nombre_Sistema`: Nombre de la aplicación o servicio.
    4.  `Descripcion`: Funcionalidades principales y objetivos de soporte de TI.
    5.  `Clasificacion_ABB_SBB`: `ABB` para conceptos de negocio/servicios genéricos o `SBB` para software físico de proveedores.
    6.  `Fabricante_Proveedor`: Fabricante u organizador técnico que brinda soporte.
    7.  `Version`: Versión instalada en producción (solo para SBB).
    8.  `Estado_Ciclo_Vida`: *Activo, En Desarrollo, En Plan de Retiro, Obsoleto*.
    9.  `Tipo_Despliegue`: *SaaS, PaaS, IaaS, On-Premises, Híbrido*.
    10. `Propietario_Negocio`: Área del negocio responsable del sistema.
    11. `Lider_Tecnico`: Responsable del mantenimiento o arquitectura de la solución.
    12. `Servicios_Negocio_Soportados`: Procesos o capacidades de negocio habilitados por este sistema.
    13. `Entidades_Datos_Consumidas ->`: Datos que lee.
    14. `Entidades_Datos_Creadas ->`: Datos que escribe o almacena en origen.

**Uso**:
- documentar portfolios de aplicaciones,
- evaluar obsolescencia,
- y trazar datos consumidos y generados por cada sistema.

### 4.3 Plantilla 3: Catálogo de Tecnología (catalogo_tecnologia_plantilla.csv)
**Objetivo**: Registrar la infraestructura de software y hardware (servidores, redes, middleware, sistemas operativos) sobre la que corren las aplicaciones de la empresa, alineada con el Modelo de Referencia Técnico de TOGAF (TRM).

*   **Entidades Metamodelo Soportadas**: *Platform Service, Logical Technology Component, Physical Technology Component*.
*   **Campos de la Plantilla**:
    1.  `ID_Tecnologia`: Identificador único (ej. TEC-ABB-001, TEC-SBB-001).
    2.  `Tipo_Elemento`: Tipo de componente tecnológico lógicos o físicos, o servicios de plataforma.
    3.  `Nombre_Tecnologia`: Nombre de la infraestructura, estándar o dispositivo.
    4.  `Descripcion`: Detalles del soporte técnico provisto.
    5.  `Clasificacion_TRM_TOGAF`: Categoría en la taxonomía TRM (ej. *Database Engine, Operating System, Application Server, Network Link, Security Engine*).
    6.  `Clasificacion_ABB_SBB`: `ABB` (ej. estándar RDBMS genérico) o `SBB` (ej. PostgreSQL 15.4 RDS).
    7.  `Clase_Estandar_Empresa`: Nivel de aprobación interna (*Approved Standard, Proposed Standard, Provisional, Phasing-Out, Retired*).
    8.  `Fabricante_Proveedor`: Proveedor tecnológico responsable de la tecnología.
    9.  `Version_Especifica`: Versión física actual.
    10. `Modelo_Hardware_Especificacion_SW`: Modelo físico del servidor o arquitectura del sistema de software.
    11. `Ubicacion_Fisica_Nube`: Dónde corre físicamente la tecnología (ej. Región AWS us-east-1, Centro de Datos Local).
    12. `Fecha_Fin_Soporte`: Fecha límite de soporte oficial provisto por el fabricante.

**Uso**:
- identificar plataformas, estándares y componentes físicos de infraestructura,
- validar compatibilidad con la Base de Información de Estándares (SIB),
- y controlar riesgos de soporte y obsolescencia.

### 4.4 Plantilla 4: Catálogo de Requerimientos de Arquitectura (catalogo_requerimientos_plantilla.csv)
**Objetivo**: Capturar y mantener la trazabilidad de los requerimientos técnicos y no funcionales que la solución del proveedor debe cumplir para ser calificada como conforme dentro del gobierno de arquitectura empresarial.

*   **Entidades Metamodelo Soportadas**: *Requirement*.
*   **Campos de la Plantilla**:
    1.  `ID_Requerimiento`: Identificador del requerimiento (ej. REQ-001).
    2.  `Nombre_Requerimiento`: Título claro y conciso del requerimiento.
    3.  `Descripcion_Detallada`: Declaración cuantitativa de la necesidad técnica o de negocio (ej. tiempo de respuesta, algoritmo de cifrado, redundancia física).
    4.  `Tipo_Requerimiento`: *Negocio, No Funcional - Seguridad, No Funcional - Disponibilidad, No Funcional - Rendimiento, Técnico - Integración, Transición*.
    5.  `Prioridad`: Priorización (*Alta, Media, Baja*).
    6.  `Estado_Actual`: *Identificado, Analizado, Aprobado, Implementado, Validado*.
    7.  `Origen_Solicitante`: Área o rol técnico solicitante (ej. Oficina de Seguridad, Infraestructura).
    8.  `Objetivo_Negocio_Relacionado ->`: Vínculo con los objetivos estratégicos corporativos.
    9.  `Componentes_Sistemas_Afectados ->`: IDs de elementos de datos, sistemas o tecnologías asociados (trazabilidad).
    10. `Metricas_De_Cumplimiento`: Criterio cuantificable que usará el área de arquitectura para verificar la conformidad de la solución.

**Uso**:
- asegurar trazabilidad entre necesidades de negocio y cumplimiento tecnológico,
- y definir criterios de aprobación y validación.

---

## 5. Matrices del SDA

### 5.1 Plantilla 5: Matriz de Integraciones (`matriz_integraciones_plantilla.csv`)
**Objetivo**: Esta matriz documenta el inventario de servicios y canales de comunicación entre aplicaciones y componentes de terceros. Mapea la relación entre los componentes lógicos (ABBs) y los componentes de despliegue real (SBB).

* **Campos Principales**:
  - `ID_Integracion`: Identificador unico (ej. `INT-001`).
  - `Nombre_Integracion`: Nombre funcional del servicio o interacción.
  - `Sistema_Origen_ABB ->` / `Sistema_Origen_SBB ->`: Componente emisor (lógico y físico).
  - `Sistema_Destino_ABB ->` / `Sistema_Destino_SBB ->`: Componente receptor / backend (lógico y físico).
  - `Tipo_Integracion`: Protocolo o formato (SOAP, REST, ETL, Batch, Event-Driven/Platform Event).
  - `Patron_Sincronia`: Sincronico (Req-Reply), Asincrónico, Publish-Subscribe.
  - `Endpoint_Origen_Exposicion`: URL o recurso expuesto por el origen.
  - `Endpoint_Destino_Consumo`: URL de consumo en el bus o backend (ej. endpoint ESB/COBIS).
  - `Mecanismo_Autenticacion`: OAuth 2.0, Basic Auth, Mutual TLS, Custom Header.
  - `Frecuencia_Volumen`: Estimación de transacciones por dia / hora pico.
  - `Estado_CicloVida`: Baseline, Target, Transition, Phasing-Out.

**Qué permite**:
- conocer cómo interactúan los sistemas,
- identificar dependencias y rutas de integración,
- y evaluar riesgos de seguridad, rendimiento y compatibilidad.

### 5.2 Plantilla 6: Matriz de Flujos de Datos (`matriz_flujos_datos_plantilla.csv`)
**Objetivo**: Con base en el *Data Dissemination Diagram* y la *Information Exchange Matrix* de TOGAF, especifica qué datos de negocio se mueven, con qué frecuencia, bajo qué operaciones y con qué nivel de seguridad.

**Campos Principales**:
  - `ID_Flujo_Datos`: Identificador unico del flujo (ej. `DFLOW-001`).
  - `Nombre_Flujo`: Descripcion del proceso de transferencia.
  - `Entidad_Dato_Logica ->`: Entidad conceptual/lógica (ej. *Cliente / Afiliado*, *Transaccion*).
  - `Componente_Dato_Fisico ->`: Tabla, vista, objeto CRM o BigObject donde se materializa.
  - `Rol_Dato`: Maestro (Familia A), Transaccional (Familia B), Log/Histórico (Familia C).
  - `Sistema_Emisor_Origen ->` / `Sistema_Receptor_Destino ->`: Aplicaciones origen y destino.
  - `Operacion_CRUD`: Create, Read, Update, Delete.
  - `Tipo_Carga_Mecanismo`: Push por registro, Carga Masiva (DataLoader), Delta Batch.
  - `Transformacion_Homologacion`: Reglas de mapeo o tablas de homologación aplicadas en el trayecto.
  - `Frecuencia_Ejecucion`: Tiempo real, Diario nocturno, Event-Driven.
  - `Sensibilidad_Seguridad`: Clasificación de seguridad (PII, Confidencial, Público).

**Qué permite**:
- mapear la movilidad real de la información,
- controlar datos críticos y su tratamiento,
- y detectar problemas de integridad, seguridad o sincronización.

### 5.3 Plantilla 7: Matriz de Transición de Arquitectura y Trazabilidad (`matriz_transicion_arquitectura_plantilla.csv`)
**Objetivo**: Basada en el *Transition Architecture State Evolution Table* y la tabla de *Increments* de TOGAF E/F, permite llevar el control estricto de la evolucion de los artefactos a lo largo de los *Plateaus* o estados temporales de transición.

* **Campos Principales**:
  - `ID_Elemento`: Identificador del componente o servicio afectado.
  - `Nombre_Elemento ->`: Nombre del artefacto de arquitectura.
  - `Dominio_Arquitectura`: Negocio, Datos, Aplicación, Tecnología.
  - `Estado_Baseline_AsIs`: Estado en la operación previa / legacy.
  - `Estado_Transicion_1_Cert`: Estado en el primer hito de entrega (ej. Certificacion/Sandbox).
  - `Estado_Transicion_2_Pilot`: Estado en el segundo hito (ej. Piloto/Go-Live Remediation).
  - `Estado_Target_ToBe`: Estado final deseado en producción.
  - `Tipo_Accion_Cambio`: Taxonomía TOGAF/ArchiMate: *New* (Nuevo), *Retain* (Mantener), *Replace* (Reemplazar), *Retire* (Retirar), *Transition* (En transición).
  - `Paquete_Trabajo_Proyecto ->`: Work Package o proyecto responsable del cambio.
  - `Justificacion_Brecha_Gap`: Brecha o necesidad técnica/de negocio que motiva el cambio.
  - `Criterio_Salida_Gate`: Gate de calidad/KPI para aprobar la salida a la siguiente fase.
  - `Riesgo_Asociado`: Riesgo operativo durante la transición.

**Qué permite**:
- controlar la evolución de activos y soluciones,
- visualizar cambios por hito o transición,
- y gestionar la adopción incremental de nuevas arquitecturas.

### 5.4 Plantilla 8: Matriz de Brechas, Soluciones y Gobierno (`matriz_brechas_soluciones_gobierno_plantilla.csv`)
**Objetivo**: Alineada con la *Consolidated Gaps, Solutions, and Dependencies Matrix* y el *Governance Log* de TOGAF, permite auditar que cada brecha identificada tenga una solución tecnologica concreta (SBB), un ROI claro y la aprobación del Comité de Arquitectura.

* **Campos Principales**:
  - `ID_Brecha_Gap`: Identificador de la brecha (ej. `GAP-DAT-01`).
  - `Dominio_Afectado`: Negocio, Datos, Aplicacion, Tecnología, Gobierno.
  - `Descripcion_Brecha`: Deficiencia o diferencia entre el estado actual y el objetivo.
  - `Solucion_Propuesta_SBB ->`: Componente especifico o producto que resuelve la brecha.
  - `Paquete_Trabajo_Asociado ->`: Proyecto encargado de la implementación.
  - `Dependencias_Tecnicas`: Requisitos previos o bloqueos con otros componentes.
  - `Prioridad_Negocio`: Alta, Media, Baja.
  - `Valor_Negocio_ROI`: Beneficio cuantificable o cualitativo.
  - `Mecanismo_Gobierno_Compliance`: Instancia de aprobación (Architecture Board, Compliance Review, SLA Audit).
  - `Estado_Aprobacion`: Propuesto, En Revision, Aprobado, Exceptuado.

**Qué permite**:
- cerrar la brecha entre el estado actual y el objetivo,
- vincular soluciones concretas con proyectos y gobernanza,
- y asegurar que cada decisión tiene justificación y aprobación formal.

---

## 6. Flujo de gobierno y alimentación del repositorio (proveedores tecnológicos)

La entrega, diligenciamiento y carga del SDA sigue un ciclo objetivo:

```
 [1. Asignación]            [2. Diligenciamiento]         [3. Evaluación Compliance]         [4. Carga Repositorio]     [5. ]
 Arquitectura entrega  -->  Proveedor completa CSVs  -->  Comité de Arquitectura       -->   Modelado EA / Archi        (proc) documentación 
 plantillas al proveedor    (SBB, Endpoints, Gaps)        evalúa estándares y riesgos        Trazabilidad End-to-End    técnica
```

1. **Entrega de Plantillas**: El equipo de arquitectura entrega el conjunto de las 8 plantillas CSV al proveedor al inicio de la fase de diseño o construcción.
2. **Diligenciamiento por el Proveedor**: El proveedor completa la información técnica detallando componentes físicos, integraciones, endpoints reales, flujos de datos y la matriz de transición de sós entregables.
3. **Validacion de Gobierno (Architecture Board)**: 
   - La Mesa de Arquitectura revisa la información frente a la Base de Información de Estándares (SIB) de la empresa y evalúan los criterios de salida (*Gates*) de la matriz de transición.
   - Verifica versiones, clasificación de estándares, riesgos y cumplimiento de métricas.
4. **Carga en el Repositorio de Arquitectura**: 
   - Los archivos CSV planos se importan en la herramienta de modelado (ej. ArchiMate via CSV Importer / Enterprise Architect / iServer) para generar automaticamente los diagramas de interacción, diagramas de despliegue y matrices de trazabilidad de cambios.
   - Los SBB son vinculados con los ABBs definidos por la organización.
4. **Carga e integración al repositorio**
   - Los archivos son importados al repositorio de arquitectura.
   - Los SBB son vinculados con los ABBs definidos por la organización.
5. **Gobernanza y trazabilidad**
   - Se mantiene evidencia documental de decisiones, aprobaciones, brechas y requisitos.

Este flujo asegura una trazabilidad de extremo a extremo, útil para auditoría técnica, seguridad, cumplimiento y transformación de arquitectura.

---

## 7. Principios de uso del SDA

El SDA debe usarse bajo estos principios:

- **Consistencia**: todos los activos deben registrarse con nomenclatura y campos definidos.
- **Trazabilidad**: cada solución debe relacionarse con requerimientos, datos, sistemas y tecnologías.
- **Conformidad**: los componentes deben alinearse a estándares aprobados y políticos de gobierno.
- **Rigor documental**: la evidencia debe ser clara, completa y mantenible.
- **Gobernanza**: las decisiones deben registrarse y revisarse en comités o instancias de arquitectura.

---

## 8. Resumen ejecutivo

El SDA es el mecanismo de formalización y gobierno de la arquitectura empresarial de la organización. A través de cuatro catálogos base y cuatro matrices de trazabilidad, se logra:

- un inventario completo de datos, aplicaciones y tecnología,
- la documentación de integraciones y flujos de información,
- la gestión de transiciones de arquitectura,
- y la relación explícita entre brechas, soluciones y decisiones de gobierno.

La combinación de TOGAF y ArchiMate permite que el repositorio no solo documente la arquitectura, sino que también la haga operativa, auditable y alineada con la estrategia de la empresa.

---

## 9. Estructura resumida de archivos

| Categoría | Archivo                                            | Propósito                                 |
|:----------|:---------------------------------------------------|:------------------------------------------|
| Catálogos | `catalogo_datos_plantilla.csv`                     | Datos lógicos y físicos                   |
| Catálogos | `catalogo_sistemas_plantilla.csv`                  | Aplicaciones y componentes                |
| Catálogos | `catalogo_tecnologia_plantilla.csv`                | Infraestructura y estándares              |
| Catálogos | `catalogo_requerimientos_plantilla.csv`            | Requerimientos y criterios de conformidad |
| Matrices  | `matriz_integraciones_plantilla.csv`               | Interfaces y protocolos                   |
| Matrices  | `matriz_flujos_datos_plantilla.csv`                | Transferencias de información             |
| Matrices  | `matriz_transicion_arquitectura_plantilla.csv`     | Evolución temporal y cambios              |
| Matrices  | `matriz_brechas_soluciones_gobierno_plantilla.csv` | Brechas, soluciones y aprobación          |

---

## 10. Cierre

El SDA no es solo una colección de plantillas CSV; es la base operativa para gobernar la arquitectura de la organización, asegurar la calidad de las soluciones y mantener la trazabilidad entre el diseño, la implementación y la operación.

Su valor real se materializa cuando cada proveedor tecnológico entrega información estandarizada, validada y conectada al repositorio de arquitectura de la empresa.
