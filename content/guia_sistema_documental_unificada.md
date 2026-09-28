# Guía Unificada del Sistema Documental de Arquitectura (SDA)
## Marco de trabajo basado en TOGAF ADM y ArchiMate 3.1

**Uso interno y para distribución a proveedores tecnológicos**

--- 

## Vision General del SDA

El **Sistema Documental de Arquitectura (SDA)** constituye la estructura central del **Repositorio de Arquitectura** de la organización. Su objetivo es gobernar, visibilizar y mantener la trazabilidad de los componentes de negocio, datos, aplicaciones e infraestructura, integrando tanto la vision lógica (**Architecture Building Blocks - ABBs**) como la solución física entregada por los proveedores tecnológicos (**Solution Building Blocks - SBBs**).

Para garantizar un gobierno integral de punta a punta, el SDA se organiza en tres capas de plantillas estandarizadoras en formato CSV:

1. **Catalogos de Inventario Base** (Poblacion de elementos unicos):
   - `catalogo_datos_plantilla.csv`: Entidades de datos lógicas y componentes de almacenamiento físicos.
   - `catalogo_sistemas_plantilla.csv`: Servicios de SI, componentes lógicos y paquetes de software.
   - `catalogo_tecnologia_plantilla.csv`: Plataformas de software, servidores, redes y hardware.
   - `catalogo_requerimientos_plantilla.csv`: Requerimientos funcionales, no funcionales y restricciones.

2. **Matrices de Relacion e Integracion** (Interacciones y dinamica de datos):
   - `matriz_integraciones_plantilla.csv`: Mapeo de interfaces de comunicación, protocolos (SOAP/REST/ETL) y endpoints salientes/entrantes.
   - `matriz_flujos_datos_plantilla.csv`: Trazabilidad del flujo de información, operaciones CRUD, mecanismos de carga e intercambios entre sistemas.

3. **Vistas de Cambio, Transicion y Gobierno** (Trazabilidad temporal y cumplimiento):
   - `matriz_transicion_arquitectura_plantilla.csv`: Evolucion incremental estado por estado (*Baseline*, *Transicion 1*, *Transicion 2*, *Target*) con acciones de cambio (*New*, *Retain*, *Replace*, *Retire*).
   - `matriz_brechas_soluciones_gobierno_plantilla.csv`: Trazabilidad entre brechas (*Gaps*), soluciones (*SBBs*), paquetes de trabajo (*Work Packages*) y comites de gobierno (*Architecture Board*).

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

El repositorio de arquitectura centraliza conocimiento de la organización en las siguientes áreas:

1. **Metamodelo de arquitectura**: taxonomía de elementos y relaciones.
2. **Panorama de arquitectura**: visión actual y futura del negocio, sistema y tecnología.
3. **Base de información de estándares (SIB)**: tecnologías aprobadas, estándares y su estado de ciclo de vida.
4. **Biblioteca de referencia**: plantillas, directrices, estándares y patrones reutilizables.
5. **Repositorio de requerimientos**: necesidades técnicas, funcionales y no funcionales.
6. **Panorama de soluciones**: soluciones físicas implementadas y operadas.
7. **Bitácora de gobierno**: decisiones, aprobaciones y auditorías.

### 2.3 Metamodelo de contenido

El metamodelo de contenido organiza la arquitectura en dominios clave:
- negocio,
- datos,
- aplicaciones,
- tecnología,
- requerimientos,
- y gobierno.

Los archivos del SDA alimentan este metamodelo y permiten construir trazabilidad entre elementos lógicos, físicos y de transición.

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

### 4.1 Catálogo de Datos
**Objetivo**: identificar activos de información y sus componentes lógicos y físicos.

**Entidades principales**:
- Data Entity
- Logical Data Component
- Physical Data Component

**Campos clave**:
- `ID_Elemento`
- `Tipo_Elemento`
- `Nombre`
- `Descripcion`
- `Clasificacion_ABB_SBB`
- `Modulo_LGC_Asociado`
- `Tecnologia_Almacenamiento`
- `Clasificacion_Seguridad`
- `Propietario_Datos`
- `Origen_Registro_Sistema`
- `Volumetria_Estimada`
- `Frecuencia_Actualizacion`

**Uso**:
- definir qué datos existen,
- dónde se materializan,
- quién los administra,
- y qué nivel de sensibilidad tienen.

### 4.2 Catálogo de Sistemas y Componentes
**Objetivo**: mantener el inventario de aplicaciones y servicios de tecnología.

**Entidades principales**:
- Information System Service
- Logical Application Component
- Physical Application Component

**Campos clave**:
- `ID_Componente`
- `Tipo_Elemento`
- `Nombre_Sistema`
- `Descripcion`
- `Clasificacion_ABB_SBB`
- `Fabricante_Proveedor`
- `Version`
- `Estado_Ciclo_Vida`
- `Tipo_Despliegue`
- `Propietario_Negocio`
- `Lider_Tecnico`
- `Servicios_Negocio_Soportados`
- `Entidades_Datos_Consumidas`
- `Entidades_Datos_Creadas`

**Uso**:
- documentar portfolios de aplicaciones,
- evaluar obsolescencia,
- y trazar datos consumidos y generados por cada sistema.

### 4.3 Catálogo de Tecnología
**Objetivo**: registrar infraestructura de software y hardware que soporta la operación de las soluciones.

**Entidades principales**:
- Platform Service
- Logical Technology Component
- Physical Technology Component

**Campos clave**:
- `ID_Tecnologia`
- `Tipo_Elemento`
- `Nombre_Tecnologia`
- `Descripcion`
- `Clasificacion_TRM_TOGAF`
- `Clasificacion_ABB_SBB`
- `Clase_Estandar_Empresa`
- `Fabricante_Proveedor`
- `Version_Especifica`
- `Modelo_Hardware_Especificacion_SW`
- `Ubicacion_Fisica_Nube`
- `Fecha_Fin_Soporte`

**Uso**:
- identificar plataformas, estándares y componentes físicos de infraestructura,
- validar compatibilidad con la Base de Información de Estándares (SIB),
- y controlar riesgos de soporte y obsolescencia.

### 4.4 Catálogo de Requerimientos de Arquitectura
**Objetivo**: capturar requerimientos funcionales, no funcionales y técnicos que deben cumplir las soluciones.

**Entidades principales**:
- Requirement

**Campos clave**:
- `ID_Requerimiento`
- `Nombre_Requerimiento`
- `Descripcion_Detallada`
- `Tipo_Requerimiento`
- `Prioridad`
- `Estado_Actual`
- `Origen_Solicitante`
- `Objetivo_Negocio_Relacionado`
- `Componentes_Sistemas_Afectados`
- `Metricas_De_Cumplimiento`

**Uso**:
- asegurar trazabilidad entre necesidades de negocio y cumplimiento tecnológico,
- y definir criterios de aprobación y validación.

---

## 5. Matrices del SDA

### 5.1 Matriz de Integraciones
**Objetivo**: registrar interfaces, protocolos y mecanismos de comunicación entre sistemas y componentes de terceros.

**Campos principales**:
- `ID_Integracion`
- `Nombre_Integracion`
- `Sistema_Origen_ABB` / `Sistema_Origen_SBB`
- `Sistema_Destino_ABB` / `Sistema_Destino_SBB`
- `Tipo_Integracion`
- `Patron_Sincronia`
- `Endpoint_Origen_Exposicion`
- `Endpoint_Destino_Consumo`
- `Mecanismo_Autenticacion`
- `Frecuencia_Volumen`
- `Estado_CicloVida`

**Qué permite**:
- conocer cómo interactúan los sistemas,
- identificar dependencias y rutas de integración,
- y evaluar riesgos de seguridad, rendimiento y compatibilidad.

### 5.2 Matriz de Flujos de Datos
**Objetivo**: documentar el movimiento de información entre sistemas y su tratamiento en términos de operación, seguridad y frecuencia.

**Campos principales**:
- `ID_Flujo_Datos`
- `Nombre_Flujo`
- `Entidad_Dato_Logica`
- `Componente_Dato_Fisico`
- `Rol_Dato`
- `Sistema_Emisor_Origen` / `Sistema_Receptor_Destino`
- `Operacion_CRUD`
- `Tipo_Carga_Mecanismo`
- `Transformacion_Homologacion`
- `Frecuencia_Ejecucion`
- `Sensibilidad_Seguridad`

**Qué permite**:
- mapear la movilidad real de la información,
- controlar datos críticos y su tratamiento,
- y detectar problemas de integridad, seguridad o sincronización.

### 5.3 Matriz de Transición de Arquitectura
**Objetivo**: mostrar el estado de cada elemento a lo largo del tiempo desde el baseline hasta el target.

**Campos principales**:
- `ID_Elemento`
- `Nombre_Elemento`
- `Dominio_Arquitectura`
- `Estado_Baseline_AsIs`
- `Estado_Transicion_1_Cert`
- `Estado_Transicion_2_Pilot`
- `Estado_Target_ToBe`
- `Tipo_Accion_Cambio`
- `Paquete_Trabajo_Proyecto`
- `Justificacion_Brecha_Gap`
- `Criterio_Salida_Gate`
- `Riesgo_Asociado`

**Qué permite**:
- controlar la evolución de activos y soluciones,
- visualizar cambios por hito o transición,
- y gestionar la adopción incremental de nuevas arquitecturas.

### 5.4 Matriz de Brechas, Soluciones y Gobierno
**Objetivo**: asegurar que cada brecha tenga una solución, responsable de ejecución y estado de aprobación.

**Campos principales**:
- `ID_Brecha_Gap`
- `Dominio_Afectado`
- `Descripcion_Brecha`
- `Solucion_Propuesta_SBB`
- `Paquete_Trabajo_Asociado`
- `Dependencias_Tecnicas`
- `Prioridad_Negocio`
- `Valor_Negocio_ROI`
- `Mecanismo_Gobierno_Compliance`
- `Estado_Aprobacion`

**Qué permite**:
- cerrar la brecha entre el estado actual y el objetivo,
- vincular soluciones concretas con proyectos y gobernanza,
- y asegurar que cada decisión tiene justificación y aprobación formal.

---

## 6. Flujo de gobierno y alimentación del repositorio

La entrega, diligenciamiento y carga del SDA sigue un ciclo claro:

1. **Entrega de plantillas**
   - El equipo de arquitectura entrega el conjunto de plantillas CSV al proveedor tecnológico.

2. **Diligenciamiento por el proveedor**
   - El proveedor documenta los SBBs físicos y sus componentes asociados.
   - Incluye integraciones reales, endpoints, flujos de datos, transiciones y brechas.

3. **Evaluación de conformidad**
   - La Mesa de Arquitectura revisa la información frente a la Base de Información de Estándares (SIB).
   - Verifica versiones, clasificación de estándares, riesgos y cumplimiento de métricas.

4. **Carga e integración al repositorio**
   - Los archivos sont importados al repositorio de arquitectura.
   - Los SBBs son vinculados con los ABBs definidos por la organización.

5. **Gobernanza y trazabilidad**
   - Se mantiene evidencia documental de decisiones, aprobaciones, brechas y requisitos.

Este flujo asegura una trazabilidad de extremo a extremo, útil para auditoría técnica, seguridad, cumplimiento y transformación de arquitectura.

---

## 6.1. Flujo Operativo para Proveedores Tecnológicos y Gobierno

```
 [1. Asignacion]           [2. Diligenciamiento]         [3. Evaluacion Compliance]         [4. Carga Repositorio]
 Arquitectura entrega  -->  Proveedor completa CSVs  -->  Comite de Arquitectura       -->  Modelado EA / Archi
 plantillas al proveedor    (SBBs, Endpoints, Gaps)       evalua estandares y riesgos         Trazabilidad End-to-End
```

1. **Entrega de Plantillas**: El equipo de arquitectura entrega el kit de las 8 plantillas CSV al proveedor al inicio de la fase de disenio o construccion.
2. **Diligenciamiento por el Proveedor**: El proveedor completa la información tecnica detallando componentes físicos, integraciones, endpoints reales, flujos de datos y la matriz de transición de sós entregables.
3. **Validacion de Gobierno (Architecture Board)**: Se verifica la conformidad contra la Base de Estandares (*Standards Information Base - SIB*) de la empresa y se evaluan los criterios de salida (*Gates*) de la matriz de transición.
4. **Carga en el Repositorio de Arquitectura**: Los archivos CSV planos se importan en la herramienta de modelado (ej. ArchiMate via CSV Importer / Enterprise Architect / iServer) para generar automaticamente los diagramas de interaccion, diagramas de despliegue y matrices de trazabilidad de cambios.

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

| Categoría | Archivo | Propósito |
| :--- | :--- | :--- |
| Catálogos | `catalogo_datos_plantilla.csv` | Datos lógicos y físicos |
| Catálogos | `catalogo_sistemas_plantilla.csv` | Aplicaciones y componentes |
| Catálogos | `catalogo_tecnologia_plantilla.csv` | Infraestructura y estándares |
| Catálogos | `catalogo_requerimientos_plantilla.csv` | Requerimientos y criterios de conformidad |
| Matrices | `matriz_integraciones_plantilla.csv` | Interfaces y protocolos |
| Matrices | `matriz_flujos_datos_plantilla.csv` | Transferencias de información |
| Matrices | `matriz_transicion_arquitectura_plantilla.csv` | Evolución temporal y cambios |
| Matrices | `matriz_brechas_soluciones_gobierno_plantilla.csv` | Brechas, soluciones y aprobación |

---

## 10. Cierre

El SDA no es solo una colección de plantillas CSV; es la base operativa para gobernar la arquitectura de la organización, asegurar la calidad de las soluciones y mantener la trazabilidad entre el diseño, la implementación y la operación.

Su valor real se materializa cuando cada proveedor tecnológico entrega información estandarizada, validada y conectada al repositorio de arquitectura de la empresa.
