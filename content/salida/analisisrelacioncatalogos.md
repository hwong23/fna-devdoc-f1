Análisis **`catalogo_datos.csv`** y **`catalogo_sistemas.csv`**, y relación entre el dominio de datos y el dominio de aplicaciones/sistemas.

El sistema documental articula esta relación en dos niveles de abstracción según TOGAF/ArchiMate:
1. **Nivel Lógico (ABB)**: Relación entre componentes lógicos de datos (*Logical Data Components*), entidades de datos y módulos/servicios lógicos de aplicación.
2. **Nivel Físico (SBB y Servicios)**: Relación entre la estructura física de almacenamiento (Objetos Salesforce, Big Objects, DLO de Data Cloud, Tablas) y los componentes de software (OmniScripts, Integration Procedures, Clases Apex, Servicios REST y Sistemas Externos).

---

### Tabla 1: Mapeo Resumen Lógico (ABB de Datos vs. ABB y Módulos de Aplicación)
Muestra cómo los bloques de construcción de datos abstractos son consumidos y gestionados por las capacidades lógicas de aplicación.

| ID Datos ABB    | Componente Lógico de Datos (ABB)              | Entidades de Datos Asociadas                                                            | Módulo/Componente de Aplicación Asociado (ABB)                                            | Sistema Primario de Origen / Registro                         |
|:----------------|:----------------------------------------------|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|:--------------------------------------------------------------|
| **DAT-ABB-001** | **Maestro de Clientes/Afiliados**             | `DAT-ENT-001` (Identificación)<br>`DAT-ENT-002` (Contacto/Dirección)                    | **APP-ABB-002** (Gestión de Clientes / Hub)<br>**APP-ABB-003** (Actualización de Cliente) | COBIS (`APP-SBB-056`) y Salesforce FNAProdNew (`APP-SBB-001`) |
| **DAT-ABB-002** | **Maestro de Empresas (PJ)**                  | `DAT-ENT-003` (Datos Laborales)<br>`DAT-ENT-004` (Identificación PJ)                    | **APP-ABB-005** (Empresa Relacionada / Persona Jurídica)                                  | COBIS (`APP-SBB-056`) y Salesforce FNAProdNew (`APP-SBB-001`) |
| **DAT-ABB-003** | **Prospecto (Lead)**                          | Mapeado desde captura de prospectos PN/PJ                                               | **APP-ABB-001** (Gestión de Prospectos Leads PN/PJ)                                       | Salesforce FNAProdNew (`APP-SBB-001`)                         |
| **DAT-ABB-004** | **Solicitud/Trámite Comercial (Oportunidad)** | `DAT-ENT-005` (AVC)<br>`DAT-ENT-006` (Cesantías)<br>`DAT-ENT-007` (Crédito Hipotecario) | **APP-ABB-004** (Originación de Oportunidades)                                            | Salesforce FNAProdNew (`APP-SBB-001`)                         |
| **DAT-ABB-005** | **Activo/Producto del Cliente (Asset)**       | Cuentas AVC, Cesantías, Crédito Hipotecario                                             | **APP-ABB-008** (Activos / Productos del Cliente)                                         | COBIS (`APP-SBB-056`) vía Servicios REST Inbound              |
| **DAT-ABB-006** | **Log de Integración / Trazabilidad**         | Trazas WS, Histórico Listas, Histórico Estados, Causales                                | **APP-ABB-006** (Integración y Transporte)<br>**APP-ABB-007** (Trazabilidad y Logs)       | Salesforce FNAProdNew (`APP-SBB-001`), VIGIA, OLIMPIA         |
| **DAT-ABB-007** | **Transacción Histórica**                     | Movimientos transaccionales (aportes, retiros, pagos)                                   | **APP-ABB-008** (Activos / Productos del Cliente)                                         | COBIS (`APP-SBB-056`) vía REST Inbound                        |
| **DAT-ABB-008** | **Parametrización / Homologación**            | Catálogos, Parámetros, Reglas Pre-callout, Metadata                                     | **APP-ABB-006** (Integración y Transporte)                                                | Salesforce FNAProdNew (`APP-SBB-001`)                         |

---

### Tabla 2: Mapeo Físico de Componentes de Datos (SBB) vs. Componentes de Software / Sistemas
Muestra los objetos de base de datos concretos, su tecnología de almacenamiento y los componentes del sistema encargados de su lectura, escritura o persistencia.

| ID Datos SBB              | Objeto / Componente Físico de Datos (SBB)        | Tecnología de Almacenamiento   | Componentes de Aplicación (SBB) que Consumen / Procesan           | Componentes de Aplicación (SBB) que Producen / Persisten                            |
|:--------------------------|:-------------------------------------------------|:-------------------------------|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| **DAT-SBB-001**           | `Account` (Person Account `FN1_CuentaNatural`)   | Salesforce Standard Object     | `APP-SBB-005`, `APP-SBB-011`, `APP-SBB-019`, `APP-SBB-036`         | `APP-SBB-021` (IP Calificar), `APP-SBB-034` (DM Convert), `APP-SBB-041` (Gateway PN) |
| **DAT-SBB-002**           | `FN1_Ubicacion__c` (Ubicaciones)                 | Salesforce Custom Object       | `APP-SBB-005` (ActualizarCuenta), `APP-SBB-033`                    | `APP-SBB-024` (IP ActualizarCuentaGuardar), `APP-SBB-041`                            |
| **DAT-SBB-003**           | `Account` (Jurídica / Constructoras / Sucursal)  | Salesforce Standard Object     | `APP-SBB-004`, `APP-SBB-023`, `APP-SBB-030`                        | `APP-SBB-023` (IP PJEnviarCobis), `APP-SBB-034` (DM Convert PJ)                      |
| **DAT-SBB-004**           | `FN1_EmpresaRelacionada__c`                      | Salesforce Custom Object       | `APP-SBB-007` a `009` (OmniScripts Opp), `APP-SBB-030`             | `APP-SBB-026` (IP SaveOppN2), `APP-SBB-052` (Flow Sync)                              |
| **DAT-SBB-005**           | `Lead` (Persona Natural / Jurídica)              | Salesforce Standard Object     | `APP-SBB-003`, `APP-SBB-004`, `APP-SBB-016`, `APP-SBB-020`         | `APP-SBB-019` (IP-06 GuardarProspecto), `APP-SBB-022`, `APP-SBB-034`                 |
| **DAT-SBB-006**           | `FNAE_Historicos_de_estados_prospectos__c`       | Salesforce Custom Object       | Gateways de conversión en `APP-SBB-001`                            | MuleSoft (`APP-SBB-061`) / Gateways de conversión                                    |
| **DAT-SBB-007** a **009** | `Opportunity` (AVC, Cesantías, Crédito)          | Salesforce Standard Object     | `APP-SBB-011` (Hub), `APP-SBB-027` (Send), `APP-SBB-028` (Radicar) | `APP-SBB-026` (IP SaveOppN2), `APP-SBB-035` (Load DMs), `APP-SBB-045`                |
| **DAT-SBB-010**           | `FN1_Relacionado__c`                             | Salesforce Custom Object       | `APP-SBB-009` (OS Crédito), `APP-SBB-028`                          | `APP-SBB-026` (IP SaveOppN2)                                                         |
| **DAT-SBB-011**           | `FNAE_ProductoNoConforme__c`                     | Salesforce Custom Object       | `APP-SBB-052` (Flow AfterCreate)                                   | `APP-SBB-052` (Flow ProductoNoConforme_AfterCreate)                                  |
| **DAT-SBB-012**           | `Asset` (AVC, Cesantías, Crédito)                | Salesforce Standard Object     | `APP-SBB-013` (FlexCard), `APP-SBB-014`, `APP-SBB-032`             | `APP-SBB-044` (REST Inbound), `APP-SBB-029` (OriginarCuenta)                         |
| **DAT-SBB-013**           | `FN1_Transacciones__c`                           | Salesforce Custom Object       | `APP-SBB-014` (FlexCard Movimientos), `APP-SBB-032`                | `APP-SBB-044` (Servicio REST `FCCUTAVCTransService`)                                 |
| **DAT-SBB-014** / **015** | `FN1_Transacciones_bk__b` / DLO Data Cloud       | Big Object / Data Lake Object  | `APP-SBB-049` (Data Streams Data Cloud)                            | Integraciones API / Ingest API Data Cloud (`APP-SBB-049`)                            |
| **DAT-SBB-016** / **017** | `FN1_LogWs__c` / `FCC_UT_LogWsEvent__e`          | Custom Object / Platform Event | `APP-SBB-048` (LogGuard), `APP-SBB-049`                            | `APP-SBB-038` (CobisCaller), `APP-SBB-046` (LogWsTrigger)                            |
| **DAT-SBB-020** / **021** | `FN1_Historico_Listas_Inhibitorias__c` / Bloqueo | Salesforce Custom Object       | `APP-SBB-020` (IP-04), `APP-SBB-027`                               | `APP-SBB-042` (`IP04Gateway`, `FCC_UT_BizagiRestrictivasGateway`), `APP-SBB-047`     |
| **DAT-SBB-024** a **031** | Custom Settings / Custom Metadata / Tablas       | Metadata & Settings            | `APP-SBB-038`, `APP-SBB-039`, `APP-SBB-033`, `APP-SBB-020`         | Despliegue de Metadata / Administración Salesforce                                   |

---

### Tabla 3: Mapeo de Servicios del Sistema (Information System Services) y su Flujo de Datos
Resume la interacción transaccional de los **Servicios de Información (`APP-SVC`)** exponiendo qué entidades de datos consumen y cuáles producen/actualizan en los sistemas de backend y CRM.

| ID Servicio     | Servicio de Información (System Service)              | Datos Consumidos (Input)                                              | Datos Creados / Actualizados (Output / Persistencia)                      | Sistemas Involucrados                                        |
|:----------------|:------------------------------------------------------|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|:-------------------------------------------------------------|
| **APP-SVC-001** | **Creación rápida de cliente en COBIS (PN/PJ)**       | Oportunidad (`DAT-ABB-004`), Datos Afiliado/Empresa                   | Cuenta PN/PJ (`DAT-ABB-001`/`002`), Log Trazabilidad (`DAT-ABB-006`)      | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) COBIS     |
| **APP-SVC-002** | **Actualización de cliente PN en COBIS**              | Maestro de Clientes (`DAT-ABB-001`), Parametrización (`DAT-ABB-008`)  | Maestro de Clientes (`DAT-ABB-001`), Log Trazabilidad (`DAT-ABB-006`)     | Salesforce \\(\rightarrow\\) COBIS                           |
| **APP-SVC-003** | **Consulta de cliente en COBIS**                      | Prospecto (`DAT-ABB-003`), Identificación PN/PJ                       | Log Trazabilidad (`DAT-ABB-006`)                                          | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) COBIS     |
| **APP-SVC-004** | **Validación biométrica y Confronta**                 | Maestro de Clientes (`DAT-ABB-001`), Documento                        | Log Trazabilidad (`DAT-ABB-006`), Causal (`DAT-SBB-022`)                  | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) OLIMPIA   |
| **APP-SVC-005** | **Consulta de listas SARLAFT (VIGIA)**                | Prospecto (`DAT-ABB-003`), Afiliado (`DAT-ABB-001`)                   | Histórico Listas (`DAT-SBB-020`), Flags Lead/Account, Log (`DAT-ABB-006`) | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) VIGIA     |
| **APP-SVC-006** | **Relación cliente y radicación trámite hipotecario** | Oportunidad Hipotecario (`DAT-ABB-004`), Relacionados (`DAT-SBB-010`) | Estado Oportunidad (`DAT-ABB-004`), Log Trazabilidad (`DAT-ABB-006`)      | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) COBIS     |
| **APP-SVC-007** | **Originación de cuenta AVC en el core**              | Oportunidad AVC (`DAT-ABB-004`), Afiliado (`DAT-ABB-001`)             | Materialización de `Asset` AVC (`DAT-ABB-005`), Log (`DAT-ABB-006`)       | Salesforce \\(\rightarrow\\) ESB \\(\rightarrow\\) COBIS     |
| **APP-SVC-008** | **Consulta de productos y estado de cuenta**          | `Asset` (`DAT-ABB-005`), Número de Cuenta                             | Consulta en vivo de saldos/movimientos, Log (`DAT-ABB-006`)               | Salesforce \\(\leftarrow\rightarrow\\) COBIS                 |
| **APP-SVC-010** | **Recepción de productos desde COBIS (REST Inbound)** | Datos de producto y transacciones enviadas por COBIS                  | Upsert de `Asset` (`DAT-ABB-005`), Transacciones (`DAT-ABB-007`)          | COBIS \\(\rightarrow\\) Apex REST Salesforce (`APP-SBB-044`) |
| **APP-SVC-011** | **Registro de trazabilidad de integraciones**         | Events `FCC_UT_LogWsEvent__e` / `VigiaEvent__e`                       | Persistencia en `FN1_LogWs__c` (`DAT-SBB-016`)                            | Capa Interna Salesforce                                      |

---

