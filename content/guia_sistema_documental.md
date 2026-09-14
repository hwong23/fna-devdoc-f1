# SISTEMA DOCUMENTAL DE ARQUITECTURA (SDA)
## Marco de Trabajo Basado en TOGAF ADM y ArchiMate 3.1
**Para uso interno y distribución a Proveedores Tecnológicos**

---

Este documento define el **Sistema Documental de Arquitectura (SDA)** de la organización, diseñado sobre el estándar de arquitectura empresarial **TOGAF 9.2** y modelado bajo el lenguaje **ArchiMate 3.1**. El objetivo principal de este sistema es centralizar, estandarizar y gobernar la información técnica de los activos de TI para alimentar el **Repositorio de Arquitectura de la Empresa**.

Con el fin de automatizar la captura de datos desde los proveedores tecnológicos, definimos las **4 Plantillas CSV estándar** que deben ser diligenciadas de forma obligatoria para habilitar el gobierno, la conformidad y la interoperabilidad de las soluciones en nuestro ecosistema digital.

---

## 1. FUNDAMENTOS DEL SISTEMA DOCUMENTAL

El SDA se organiza en torno a tres pilares fundamentales definidos por TOGAF:
1. **Bloques de Construcción (Building Blocks)**: La distinción entre especificaciones abstractas (ABB) e implementaciones concretas (SBB).
2. **Repositorio de Arquitectura (Architecture Repository)**: Las áreas lógica y físicas donde se almacena el conocimiento arquitectónico.
3. **Metamodelo de Contenido (Content Metamodel)**: La taxonomía de entidades (datos, aplicaciones, tecnologías y requerimientos) y sus relaciones.

### 1.1 Bloques de Construcción: ABB vs. SBB
En el ciclo de desarrollo de arquitectura (ADM), los elementos se definen en dos niveles de abstracción:

*   **Architecture Building Blocks (ABBs - Bloques de Construcción de Arquitectura)**: Describen capacidades genéricas lógicas y abstractas. Son independientes de la tecnología y el proveedor (ej. *"Servicio de Motor de Base de Datos Relacional"* o *"Sistema de Gestión de Clientes"*). Definen los requerimientos de arquitectura y guían el desarrollo de los SBBs.
*   **Solution Building Blocks (SBBs - Bloques de Construcción de Solución)**: Representan componentes reales, productos comerciales, software empaquetado (COTS) o desarrollos específicos que implementan la funcionalidad del ABB (ej. *"PostgreSQL v15 RDS en AWS"* o *"Salesforce Service Cloud"*). Son específicos del proveedor y son conscientes de la configuración física de despliegue.

### 1.2 Estructura del Repositorio de Arquitectura
El Repositorio de Arquitectura de la empresa actúa como un archivo centralizado gobernado bajo las siguientes áreas de TOGAF:

1.  **Metamodelo de Arquitectura (Architecture Metamodel)**: El esquema maestro que define la taxonomía de los elementos lógicos y físicos y sus interrelaciones.
2.  **Panorama de Arquitectura (Architecture Landscape)**: El estado actual y objetivo de los activos (lógicos e implementados) de la empresa a niveles Estratégico, de Segmento y de Capacidad.
3.  **Base de Información de Estándares (SIB - Standards Information Base)**: Define las tecnologías aprobadas, estándares de la industria y la clasificación de ciclo de vida (estándar, provisorio, retirado, en obsolescencia) con las que las soluciones de los proveedores deben cumplir.
4.  **Biblioteca de Referencia (Reference Library)**: Contiene plantillas, directrices y patrones reutilizables.
5.  **Repositorio de Requerimientos (Requirements Repository)**: Centraliza los requerimientos de arquitectura, técnicos y no funcionales que guían los proyectos.
6.  **Panorama de Soluciones (Solutions Landscape)**: Registro de los SBBs implementados y desplegados por los proveedores tecnológicos.
7.  **Bitácora de Gobierno (Governance Log)**: Registro de decisiones de arquitectura, evaluaciones de conformidad y aprobaciones de proyectos.

---

## 2. METAMODELO DE CONTENIDO Y ESTRUCTURA DE PLANTILLAS CSV

Para alimentar este repositorio, los proveedores deben suministrar información estructurada en **4 Catálogos Individuales**. Cada plantilla CSV mapea directamente a entidades del metamodelo de TOGAF:

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

### Plantilla 1: Catálogo de Datos (catalogo_datos_plantilla.csv)
**Objetivo**: Identificar los activos de información de la empresa, los componentes lógicos que los agrupan (para gobernanza y seguridad) y los repositorios físicos (bases de datos, esquemas) donde se almacenan físicamente.

*   **Entidades Metamodelo Soportadas**: *Data Entity, Logical Data Component, Physical Data Component*.
*   **Campos de la Plantilla**:
    1.  `ID_Elemento`: Identificador único según nomenclatura (ej. DAT-ABB-001, DAT-SBB-001).
    2.  `Tipo_Elemento`: Debe especificarse si es un componente de datos lógico (*Logical Data Component*), un componente físico o base de datos (*Physical Data Component*) o una entidad lógica de negocio (*Data Entity*).
    3.  `Nombre`: Nombre descriptivo legible (ej. Maestro de Clientes).
    4.  `Descripcion`: Propósito del almacenamiento o definición del dominio del dato.
    5.  `Clasificacion_ABB_SBB`: Indica si corresponde a la definición abstracta de datos (`ABB`) o al producto físico implementado (`SBB`).
    6.  `Modulo_LGC_Asociado ->`: Vínculo para asociar entidades a su componente lógico.
    7.  `Tecnologia_Almacenamiento`: Motor de base de datos o almacenamiento físico utilizado (solo para SBBs).
    8.  `Clasificacion_Seguridad`: Nivel de sensibilidad del dato (*Público, Interno, Confidencial, Restringido*).
    9.  `Propietario_Datos`: Área del negocio dueña del dato.
    10. `Origen_Registro_Sistema`: Sistema de origen que se considera la "aplicación de registro" productora del dato.
    11. `Volumetria_Estimada`: Cantidad aproximada de registros.
    12. `Frecuencia_Actualizacion`: Tiempo de refresco (ej. Tiempo Real, Diario, Mensual).

---

### Plantilla 2: Catálogo de Sistemas y Componentes (catalogo_sistemas_plantilla.csv)
**Objetivo**: Mantener el inventario unificado de aplicaciones (*Application Portfolio*) y servicios de TI de la empresa. Permite identificar la obsolescencia tecnológica, el solapamiento funcional y definir el alcance de los proyectos de cambio.

*   **Entidades Metamodelo Soportadas**: *Information System Service, Logical Application Component, Physical Application Component*.
*   **Campos de la Plantilla**:
    1.  `ID_Componente`: Identificador único (ej. APP-ABB-001, APP-SBB-001).
    2.  `Tipo_Elemento`: Tipo de entidad (*Logical Application Component, Physical Application Component, Information System Service*).
    3.  `Nombre_Sistema`: Nombre de la aplicación o servicio.
    4.  `Descripcion`: Funcionalidades principales y objetivos de soporte de TI.
    5.  `Clasificacion_ABB_SBB`: `ABB` para conceptos de negocio/servicios genéricos o `SBB` para software físico de proveedores.
    6.  `Fabricante_Proveedor`: Fabricante u organizador técnico que brinda soporte.
    7.  `Version`: Versión instalada en producción (solo para SBBs).
    8.  `Estado_Ciclo_Vida`: *Activo, En Desarrollo, En Plan de Retiro, Obsoleto*.
    9.  `Tipo_Despliegue`: *SaaS, PaaS, IaaS, On-Premises, Híbrido*.
    10. `Propietario_Negocio`: Área del negocio responsable del sistema.
    11. `Lider_Tecnico`: Responsable del mantenimiento o arquitectura de la solución.
    12. `Servicios_Negocio_Soportados`: Procesos o capacidades de negocio habilitados por este sistema.
    13. `Entidades_Datos_Consumidas ->`: Datos que lee.
    14. `Entidades_Datos_Creadas ->`: Datos que escribe o almacena en origen.

---

### Plantilla 3: Catálogo de Tecnología (catalogo_tecnologia_plantilla.csv)
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

---

### Plantilla 4: Catálogo de Requerimientos de Arquitectura (catalogo_requerimientos_plantilla.csv)
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

---

## 3. FLUJO DE GOBIERNO Y ALIMENTACIÓN DEL REPOSITORIO

La distribución, diligenciamiento y carga de estas plantillas sigue un ciclo de gobierno de TI agregado:

1.  **Distribución y Solicitud**: Durante el proceso de adquisición o al inicio de un proyecto de tecnología, el equipo de Arquitectura de la empresa distribuye estas 4 plantillas CSV al proveedor técnico.
2.  **Diligenciamiento por el Proveedor**: El proveedor tecnológico completa las filas correspondientes a los **SBBs (Solution Building Blocks)** físicos:
    *   Detalla los componentes físicos de aplicación (`APP-SBB`).
    *   Detalla los componentes físicos de datos (`DAT-SBB`).
    *   Detalla las plataformas e infraestructuras físicas de software/hardware que despliega (`TEC-SBB`).
    *   Mapea cómo sus componentes físicos cumplen con los requerimientos técnicos (`REQ`).
3.  **Evaluación de Conformidad**: La Mesa de Arquitectura revisa el CSV diligenciado contra la **Base de Información de Estándares (SIB)** de la empresa:
    *   Verifica que las versiones de BD, SO e infraestructura estén marcadas como *Approved Standard*.
    *   Revisa el cumplimiento de métricas definidas en el catálogo de requerimientos.
4.  **Carga e Integración**: Una vez aprobado, el área de arquitectura carga los archivos CSV en el **Repositorio de Arquitectura Empresarial**, enlazando los **SBBs** provistos por el proveedor tecnológico con los **ABBs** (procesos de negocio, servicios lógicos de datos y aplicación) definidos previamente por la organización.

Este flujo garantiza una trazabilidad de extremo a extremo, facilitando la auditoría técnica, la mitigación de riesgos operativos y una transición ágil hacia nuevas arquitecturas empresariales.
