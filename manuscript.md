---
title: Manuscript Title
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2023-01-11'
author-meta:
- John Doe
- Jane Roe
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Manuscript Title" />
  <meta name="citation_title" content="Manuscript Title" />
  <meta property="og:title" content="Manuscript Title" />
  <meta property="twitter:title" content="Manuscript Title" />
  <meta name="dc.date" content="2023-01-11" />
  <meta name="citation_publication_date" content="2023-01-11" />
  <meta property="article:published_time" content="2023-01-11" />
  <meta name="dc.modified" content="2023-01-11T16:45:07+00:00" />
  <meta property="article:modified_time" content="2023-01-11T16:45:07+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="John Doe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="twitter:creator" content="@johndoe" />
  <meta name="citation_author" content="Jane Roe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <link rel="canonical" href="https://hwong23.github.io/fna-devdoc-f1-1/" />
  <meta property="og:url" content="https://hwong23.github.io/fna-devdoc-f1-1/" />
  <meta property="twitter:url" content="https://hwong23.github.io/fna-devdoc-f1-1/" />
  <meta name="citation_fulltext_html_url" content="https://hwong23.github.io/fna-devdoc-f1-1/" />
  <meta name="citation_pdf_url" content="https://hwong23.github.io/fna-devdoc-f1-1/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://hwong23.github.io/fna-devdoc-f1-1/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://hwong23.github.io/fna-devdoc-f1-1/v/3c43184056a7e7c797e7cfd79409c113f9138d84/" />
  <meta name="manubot_html_url_versioned" content="https://hwong23.github.io/fna-devdoc-f1-1/v/3c43184056a7e7c797e7cfd79409c113f9138d84/" />
  <meta name="manubot_pdf_url_versioned" content="https://hwong23.github.io/fna-devdoc-f1-1/v/3c43184056a7e7c797e7cfd79409c113f9138d84/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...

# Fase 1: Estado SOA Actual
# Contenido de los Productos del Alcance

# Producto 1: PR1. SOA Actual
Presentar la situación general SOA del Fondo Nacionnal del Ahorro (FNA) al año 2022 - 2023 desde organizada según las vistas de arquitectura. Por tanto, la situación general SOA del Fondo está comprendida por las vistas funcional, la de información, integración y la vista tecnológoca actual en donde destacan los sistemas de información (aplicaciones) críticas para el negocio, los servicios SOA y las tecnologías y proveedores que operan en el Fondo.

## Justificación
La arquitectura, organizada por vistas, se convierte en un medio de trabajo común entre negocio y tecnología. Adicionalmente, provee un vocabulario común y un espacio de análisis sobre las decisiones de arquitectura y su impacto en el negocio.  La estructura por vistas, es un estándar de organización de arquitectura  y se sugieren las mínimas necesarias para lograr comunicar de forma efectiva las decisiones relevantes que componen la propuesta de servicios actual del Fondo.

## Contenidos
1. Descripción de la vista Funcional Actual
	* Vista de Contexto: objetivos del diagnóstico SOA, productos, áreas, y procesos FNA objeto del diagnóstico
	* Vista de Segmento del ejercicio SOA del FNA
	* Catálogo de servicios (blueprint) seleccionados FNA
		* Áreas objeto del diagnóstico SOA
		* Capacidades de negocio FNA relacionadas con servicios SOA
		* Sistemas de información, aplicaciones y servicios
		* Tipos de Servicios / Distribución de servicios SOA por tipo
	* Servicios independientes (FNA debería tener)
	* Procesos del FNA relacionados con los productos, objetivos, y áreas FNA objeto del diagnóstico SOA
	* Arquitectura de referencia SOA del FNA
1. Descripción de la vista de Información actual
	* Portafolio de aplicaciones y proveedores
	* Inventario de fuentes de datos
1. Descripción de la vista de Integración actual
	* Matriz de intercambio de información crítica del negocio
	* Entidades de negocio (información y datos) relacionadas en la integración
	* Conectores y servicios de integración
	* Inventario de servicios por tipo (negocio, utilitarios, datos… )
	* Conectores: necesidades de integración de las áreas del FNA objeto del diagnóstico SOA
	* Interrelación Entre Servicios SOA del FNA
1. Descripción de la vista Tecnológica actual
	* Listado tecnológico del inventario de servicios
1. Presentación del Método para el Análisis de Madurez SOA del FNA
	* Cuestionarios de los objetivos del análisis
	* Dimensiones del análisis (OSIMM)
	* Herramienta de diagnóstico de nivel de madurez SOA

## Criterios de Aceptación

*   Descripción de las vistas funcionales para los dominios de negocio, información, Tecnológica e integración
*   Análisis  y diagnóstico del nivel de madurez SOA

*** 

|Tema|Vista de Contexto: **Objetivos del Diagnóstico SOA y Productos, Áreas, y Procesos FNA Objeto del Diagnóstico**|
|----|---------------------------------------------------------------------------|
|Palabras clave|SOA, Contexto, Áreas, Procesos, Objetivos
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos|[N001d. Ejecución Plan de Trabajo SOA](onenote:#N001d.%20Ejecución%20Plan%20de%20Trabajo%20SOA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={45CC9047-3DB4-4CFD-BCA1-D9619F4A0C4D}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one)<br>[N003a. Procesos de Negocio FNA](onenote:#N003a.%20Procesos%20de%20Negocio%20FNA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={DAE4ECE3-B936-461D-A468-83492014F7F7}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one)|
|||

<br>

# Vista de Contexto SOA FNA (181-2020)
## Objetivos del diagnóstico SOA y Productos, Áreas Procesos FNA Objeto del Diagnóstico
La vista de contexto presenta una visión de la empresa ajustada a aquellas partes que entran en el alcance de este proyecto, 181-2020, diagnóstico SOA FNA. 

![](vistacontexto.png)

Esta vista informa al Fondo Nacional del Ahorro (FNA, en adelante) dos temas: primero, que el ejercicio actual, aunque utilice una visión empresarial, no puede abarcar a la completitud de la empresa, sino que hace foco en las partes indicadas que son relevantes según las restricciones de ejecución y de resultados esperados del proyecto. Segundo, la vista de contexto comunica las problemáticas (que a la vez son objetivos de solución) a los que le apuntarán los diagnósticos de este proyecto.

<br>

# Detalles de la Vista de Contexto SOA FNA (181-2020)
## Objetivos de la Consultoría: Problemática y Diagnósticos

La consultoría SOA (proyecto 181-2020) tratará tres problemáticas importantes de Fondo Nacional del Ahorro (FNA):

1. OBJ1. Independencia de proveedor
1. OBJ2. Flexibilidad y tiempo de mercado
1. OBJ3. Fortaleza SOA de las aplicaciones del FNA

**Nota**: Gobierno SOA del FNA lo establecemos como uno de los resultados (un producto de trabajo) que entregaremos al FNA, no como un objeto de la consultoría.

Estos objetivos fueron seleccionados según la relación valor entregado y tiempo de la consultoría, lo cual significa que estos objetivos entregan el nivel de conveniencia de los resultados que puedan desarrollarse en el tiempo de ejecución de este ejercicio.

Estos objetivos también son imporatntes porque sirven a la vez como los objetos de los diagnósticos que realizaremos en este poryecto de consultoría. 

## Productos del FNA Objetos del Diagnóstico

Esta consultoría considera como entradas para los diagnósticos a los productos de negocio del FNA siguientes:

1. Cuenta AVC (ahorro voluntario)
1. Cesantías
1. Crédito
1. Cartera

Los demás productos de negocio del FNA serán tratados únicamente cuando su relación con estos los haga relevantes según los requiera o bien un diagnóstico, o bien los objetivos de esta consultoría y del Fondo.

## Áreas de Negocio del FNA Objetos del Diagnóstico

Con base a los productos de negocio de la FNA seleccionados, las áreas del FNA que competen a esta consultoría y a los objetivos de los diagnósticos son: 

1. Vicepresidencia de Crédito
1. Vicepresidencia de Operaciones

La áreas debajo de estas, como por ejemplo, la Gerencia de Crédito Individual para el caso de la primera, o la Gerencia de Cartera, serán relacionadas en tanto se vean impactadas por un diagnóstico en marcha, o los objetivos de este consultoría y del Fondo.

### Referencia

![](OrganigramaFNA27julio.jpg)



## Procesos de Negocio Objetos del Diagnóstico

Los procesos de negocio seleccionados por este proyecto SOA son aquellos relacionados con los productos de negocio objetos de esta consultoría, por ejemplo,

1. PROC1. Administración de Cuentas y Pago de Cesantías (CSNT)
2. PROC2. Gestión Crédito
    - PROC2.1. Gestión Crédito Educativo
    - PROC2.2. Gestión Crédito Hipotecario
    - PROC2.3. Gestión Crédito Constructor
3. PROC3. Facturación y Cartera



### Referencia

![](image_2.370ae998.png)



***


|Tema|Vista de Segmento: Partes de la empresa FNA selecionados por su relación con la Vista de Contexto
|----|-------------------------------------------|
|Palabras clave|SOA, Contexto, Segmento FNA, Áreas, Procesos, Aplicaciones, Servicios
|Autor||
|Fuente||
|Vínculos|[Vista de Contexto](onenote:#N003a.%20Procesos%20de%20Negocio%20FNA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={DAE4ECE3-B936-461D-A468-83492014F7F7}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one); [N003a. Procesos de Negocio FNA](onenote:#N003a.%20Procesos%20de%20Negocio%20FNA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={DAE4ECE3-B936-461D-A468-83492014F7F7}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one)|
|||

# Vista Segmento SOA FNA 181-2020

La vista de segmento presenta la lista de las partes seleccionadas de la empresa que serán objeto de esta consultoría (proyecto 181-2020) y sobre las que se desarrollarán los procesos de análisis, brecha, hoja de ruta, y demás de esta consultoría. Es una lista filtrada de todas las partes de la empresa, y por tanto, *esta vista define el alcance horizontal del diagnóstico SOA*.

## Partes de la Empresa FNA objeto del diagnóstico SOA

Estas partes han sido seleccionadas por tener relación directa con los elementos de la vista de contexto (Ver Vista de Contexto), lo cual significa que estas partes están vinculadas, o bien con alguno de los productos de negocio o con alguno de los procesos de negocio, o con los demás elementos de la vista de contexto. 

    La "Aplicación Web Gestión Traslado" ha sido seleccionada como parte de la empresa FNA por su relación con el proceso de negocio "Aporte Cesantías".
    
    A su vez, el proceso de negocio "Aporte Cesantías" tiene que ver en forma directa con uno de los cuatro (4) productos de la vista de contexto: Cesantías. 
    
    Esto explica porqué la aplicación indicada ha sido seleccionada por el segmento de la empresa FNA objeto del diagnóstico.



Las partes de la empresa que conforman el segmento FNA a diagnosticar.

![](FNA_Arquitectura-VistaSegmentoSOAFNA181-2020.png)

* [Aporte Censatias (Business Process)](#aporte-censatias-business-process)
* [Administración de Cuentas  y Pago (Business Process)](#administración-de-cuentas--y-pago-business-process)
* [Gestión Comercial (Business Process)](#gestión-comercial-business-process)
* [Gestión de Credito (Business Process)](#gestión-de-credito-business-process)
* [Educativo (Business Process)](#educativo-business-process)
* [Procesos Misionales (Business Process)](#procesos-misionales-business-process)
* [Hipotecario (Business Process)](#hipotecario-business-process)
* [Cesantias (Business Process)](#cesantias-business-process)
* [Desembolso (Business Process)](#desembolso-business-process)
* [Facturación y Cartera (Business Process)](#facturación-y-cartera-business-process)
* [Ahorro Voluntario (Business Process)](#ahorro-voluntario-business-process)
* [Captación de Ahorro Voluntario (Business Process)](#captación-de-ahorro-voluntario-business-process)
* [Aplicación ScriptPortlet - Planilla de Consignación (Application Component)](#aplicación-scriptportlet---planilla-de-consignación-application-component)
* [Aplicación Web - Gestión Traslado (Application Component)](#aplicación-web---gestión-traslado-application-component)
* [COBIS - Cesantias (Application Component)](#cobis---cesantias-application-component)
* [Aplicación Back - Bizagi Engine (Application Component)](#aplicación-back---bizagi-engine-application-component)
* [Aplicación EJB - Credito Constructor  (Application Component)](#aplicación-ejb---credito-constructor--application-component)
* [Aplicación Web - Crédito Constructor (Application Component)](#aplicación-web---crédito-constructor-application-component)
* [Aplicación Web - Scoring (Application Component)](#aplicación-web---scoring-application-component)
* [BIZAGI (Application Component)](#bizagi-application-component)
* [COBIS - Crédito (Application Component)](#cobis---crédito-application-component)
* [Servicios Score (Technology Service)](#servicios-score-technology-service)
* [COBIS - Cartera (Application Component)](#cobis---cartera-application-component)
* [COBIS - AVC (Application Component)](#cobis---avc-application-component)
* [Servicios de Infraestructura (Technology Service)](#servicios-de-infraestructura-technology-service)
* [Transunion (Node)](#transunion-node)

<br>

**Nota**: las partes que se hagan faltan en la vista de segmento carecen de relación en los modelos de la empresa. Para que aparezcan en la vista de segmento es necesario actualizar los modelos de la empresa: modelos de negocio, procesos, servicios, aplicaciones e infraestructura.

***


|Tema|Catálogo de Servicios SOA: **Vista Funcional**
|----|-------------------------------------------------|
|Palabras clave|SOA, Áreas, Capacidades, Servicios, Conectores|
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos|[N003e. Catálogo de Servicios FNA-1a](https://stefaninilatam.sharepoint.com/:t:/s/PROYECTOARQUITECTURAE-SERVICEFNA/EXsxpcx6LllArdNIqf_wo4gBA0ZcHltkYlP5tJ4NAMNOhw?e=fRnq01); [N003e. Catálogo de Servicios FNA-4](https://stefaninilatam.sharepoint.com/:t:/s/PROYECTOARQUITECTURAE-SERVICEFNA/EQuW5UeV26lCryG3lpR68f4BxFCRNCKRKngm6dc4sRjGgQ?e=ZaFIcn)|

<br>

## Descripción de la Vista Funcional (arquitectura de referencia)
La vista funcional presenta los servicios que deben hacer parte del portafolio de servicios SOA del Fondo, por tanto, funciona a la vez como una arquitectura de referencia a la que hay que fortalecer, comparar y desarrollar y vigilar.

![](vistafuncional.png)

[Imagen. ]() Vista funcional basada en mapa de servicios.

_Fuente: elaboración propia._

>La vista funcional es importante porque presenta los _servicios SOA independientes de la tecnología y de proveedor_, alineados además con las áreas de negocio que son objeto de este diagnóstico, pero son también claves para el FNA.

<br>

Resaltamos que a partir de esta vista es necesario establecer las relaciones internas de esta arquitectura de referencia con las partes de la empresa que hacen parte de la vista de segmento (ver [N003a Vista Segmento SOA FNA](N003a%20Vista.md)) que es una colección de las partes clave de la empresa y que a la vez son relevantes para este diagnóstico. 

El ejercicio siguiente listar los conectores necesarios para conectar estas capacidades e intersectar la vista funcional con la de segmento para desarrollar el segmento de partes del FNA que le van a dar cumplimiento a esta arquitectura de referencia.

<br>

## Conectores de las Capacidades (arquitectura de referencia)
Los conectores que dinamizan la interacción entre los servicios independientes de la tecnología y de proveedor aparecen en la vista como líneas de conexión entre las capacidades de esta arquitectura de referencia.

Describimos las características de estos conectores con los siguientes ejemplos.
![](conectores.png)

[Imagen. ]() Conectores que dinamizan la interacción entre los servicios independientes.

_Fuente: elaboración propia._


|Tema|Catálogo de Servicios SOA: **Servicios SOA relevantes al diagnóstico**
|----|-------------------------------------------------|
|Palabras clave|SOA, Áreas, Capacidades, Servicios|
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos|[N003e. Catálogo de Servicios FNA-1a](https://stefaninilatam.sharepoint.com/:t:/s/PROYECTOARQUITECTURAE-SERVICEFNA/EXsxpcx6LllArdNIqf_wo4gBA0ZcHltkYlP5tJ4NAMNOhw?e=fRnq01); [N003e. Catálogo de Servicios FNA-4](https://stefaninilatam.sharepoint.com/:t:/s/PROYECTOARQUITECTURAE-SERVICEFNA/EQuW5UeV26lCryG3lpR68f4BxFCRNCKRKngm6dc4sRjGgQ?e=ZaFIcn)|

<br>

# Catálogo de Servicios FNA (blueprint)

## Capacidades de la Empresa FNA
No hay capacidades de negocio FNA en los modelos de la empresa, pero en la documentación del repositorio hay información sustituta con la que hacemos una propuesta de la vista de las capacidades FNA. Esta vista preliminar sirve para relacionar las capacidades preliminares con los servicios SOA de la empresa y con los demás elementos de la vista de segmento.

Capacidades de negocio encontradas:

1. Desarrollo de nuevos negocios
1. Gestión de Cliente
1. Administración de Recursos y Negocio
1. Entrega de Productos
1. Servicios de Cuentas
1. Gestión Financiera

_Fuente: Portafolio de Aplicaciones FNA._

<br>

## Importancia de las Capacidades y Servicios SOA (y otras partes de la empresa)
La intersección de la vista de segmento del FNA con las capacidades de negocio propuestas por este ejercicio (en color naranja abajo) resultará en la lista de servicios de negocio más importantes para la empresa dado su nivel de relación con estas capacidades.

![][embedView]

<br>

Por lo anterior, los servicios SOA del FNA más relevantes según los modelos son los indicados a continuación. De igual manera que para el Fondo, estas partes de la empresa son importantes para futuros diagnósticos y gobierno SOA.

|**Parte FNA**|**Parte Relacionada**|**Tipo**|
|-------------|---------------------|--------|
|Desarrollo de nuevos negocios|AS026-Gestión de Autenticación|**application-service**|
||AS034-ConsultarestadocuentaCartera|**application-service**|
||ASXX3-RegistrarRecaudoObligacion|**application-service**|
||COBIS|application-component|
||Servicios COBIS|application-collaboration|
|Entrega de Productos|AS026-Gestión de Autenticación|**application-service**|
||AS034-ConsultarestadocuentaCartera|**application-service**|
||ASXX3-RegistrarRecaudoObligacion|**application-service**|
||COBIS|application-component|
||Servicios COBIS|application-collaboration|
|Gestión de Cliente|AS026-Gestión de Autenticación|**application-service**|
||AS034-ConsultarestadocuentaCartera|**application-service**|
||ASXX3-RegistrarRecaudoObligacion|**application-service**|
||COBIS|application-component|
||Servicios COBIS|application-collaboration|
|Servicios de Cuentas|AS026-Gestión de Autenticación|**application-service**|
||AS034-ConsultarestadocuentaCartera|**application-service**|
||ASXX3-RegistrarRecaudoObligacion|**application-service**|
||COBIS|application-component|

_Fuente: arquitectura fna.archimate_

<br>

Las capacidades de mayor importancia para el FNA debido a su nivel superior de relación con las partes relevantes de la empresa son los siguientes

|Nombre Origen|**Destino**|**Relevancia**|
|-------------|-----------|--------------|
|Desarrollo de nuevos negocios|COBIS|**96**|
|Desarrollo de nuevos negocios|AS026-Gestión de Autenticación|8|
|Desarrollo de nuevos negocios|AS034-ConsultarestadocuentaCartera|6|
|Desarrollo de nuevos negocios|ASXX3-RegistrarRecaudoObligacion|5|
|Desarrollo de nuevos negocios|Servicios COBIS|13|
|**Total Desarrollo de nuevos negocios**||128|
|Entrega de Productos|COBIS|**96**|
|Entrega de Productos|AS026-Gestión de Autenticación|8|
|Entrega de Productos|AS034-ConsultarestadocuentaCartera|6|
|Entrega de Productos|ASXX3-RegistrarRecaudoObligacion|5|
|Entrega de Productos|Servicios COBIS|13|
|**Total Entrega de Productos**||128|
|Gestión de Cliente|COBIS|**96**|
|Gestión de Cliente|AS026-Gestión de Autenticación|8|
|Gestión de Cliente|AS034-ConsultarestadocuentaCartera|6|
|Gestión de Cliente|ASXX3-RegistrarRecaudoObligacion|5|
|Gestión de Cliente|Servicios COBIS|13|
|**Total Gestión de Cliente**||128|
|Servicios de Cuentas|COBIS|**96**|
|Servicios de Cuentas|AS026-Gestión de Autenticación|8|
|Servicios de Cuentas|AS034-ConsultarestadocuentaCartera|6|
|Servicios de Cuentas|ASXX3-RegistrarRecaudoObligacion|5|
|**Total Servicios de Cuentas**||115|

_Fuente: arquitectura fna.archimate_

<br>

-----

[embedView]: FNA_Arquitectura-Vista%20de%20Capacidades%20FNA.png


# Areas de Negocio FNA

|Tema|Catálogo de Servicios SOA: **Relación de Áreas de Negocio FNA y Servicios SOA**|
|----|-------------------------------------------|
|Palabras clave|SOA, Áreas de Negocio, Procesos
|Autor||
|Fuente|Modelos de arquitectura FNA |
|Vínculos|[Vista de Contexto](onenote:#N003a.%20Procesos%20de%20Negocio%20FNA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={DAE4ECE3-B936-461D-A468-83492014F7F7}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one); [N003a. Procesos de Negocio FNA](onenote:#N003a.%20Procesos%20de%20Negocio%20FNA&section-id={F3AC64B8-D6FF-47C7-ABBE-A2B4B6510F0F}&page-id={DAE4ECE3-B936-461D-A468-83492014F7F7}&end&base-path=https://uniandes-my.sharepoint.com/personal/ha_wong10_uniandes_edu_co/Documents/Blocs%20de%20notas/Harry%20Alfredo%20@%20Work/SOA/Trabajo%20SOA.one)|
|||

En los modelos analizados (Anexo 2) no se evidencia relación de las áreas de negocio del FNA con otros elementos de la vista de segmento. Los modelos actuales no registran la relación de las áreas con los procesos de negocio (misionales, estratégicos o de soporte, ni con los seleccionados para el diagnóstico), aplicaciones ni con servicios SOA. 

**Importante**: si falta esta relación en los modelos, no hay forma de conocer ni gestionar la demanda de los servicios SOA del Fondo, y si estos responde a necesidades de negocio, o de operación, o de tecnología, o de alguna otra área o proceso.

La única relación encontrada es la de algunas áreas de negocio del FNA con el proceso de Legalización.


![Vista][embedView]
_Fuente: ae_fna.archimate, ae_fna_as_is.archimate, ae_fna_tobe.archimate._

<br>

Las áreas de negocio que sí están modeladas (Anexo 1) no son representativas. Razón por la cual no tienen relación con los elementos relevantes de la empresa ni de este diagnóstico. 

## Anexo 1. Áreas FNA Modeladas
|Name|Type|
|--------|--------|
|1\. Cargue de insumo|business-function|
|10\. Toma de Firmas Notariales|business-function|
|11\. Validar estado Documental para Desembolso|business-function|
|12\. Seguimiento de Registro|business-function|
|13\. Consolidar carpeta Legal|business-function|
|2\. Consulta de Documento|business-function|
|3\. Estudio Preliminar Títulos|business-function|
|4\. Análisis Previo - Análisis de capacidad de pagos|business-function|
|5\. Consecución de Documentos|business-function|
|6\. Recibir documentos|business-function|
|7\. Avalúo Comercial|business-function|
|8\. Estudio de Títulos – Imprimible|business-function|
|9\. Elaboración de Minuta y Reparto Notarial|business-function|
|Aplicacion de Negocio|business-function|
|Aplicacion de Negocio (copy)|business-function|
|Business Function|business-function|
|FN1. Vicepresidencia de Crédito|business-function|
|FN2. Vicepresidencia de Operaciones.|business-function|
|Otras Áreas FNA|business-function|
|Servicio de Negocio|business-function|
|Servicio de Negocio (copy)|business-function|
|Versión Aplicación|business-function|
|Versión Aplicación (copy)|business-function|
|Versiones Del Servicio|business-function|
|Versiones Del Servicio|business-function|

<br>

## Anexo 2. Modelos Analizados
* 2015-06-01 modelo arquitectura togaf - fna banca digital v6.archimate
* aa002 - cobis ahorro voluntario.archimate
* aa003-cobis cesantias.archimate
* aa005-cobis cartera.archimate
* aa006-cobis tramites.archimate
* aa015-cobis clientes.archimate
* aa020-banca virtual.archimate
* aa021-fondo en linea.archimate
* aa074-fondo en linea personal.archimate
* **aa091-cobis cx.archimate**
* **ae_fna.archimate**
* **ae_fna_as_is.archimate**
* ae_fna_tobe.archimate
* arquitectura banca digital v4.archimate
* **arquitectura fna.archimate**
* arquitectura movil_v1.archimate
* arquitectura movil_v2.archimate
* fna_proyectos v2.0.archimate
* information_architecture_bi_ba_md_archixml.archimate
* ivr.archimate
* pa0003-pki.archimate
* workmanager.archimate

----

[embedView]: FNA_Arquitectura-Areas%20de%20Negocio%20FNA.png


|Tema|Catálogo de Servicios: **Sistemas de información, Aplicaciones y Servicios**
|----|-------------------------------------------------|
|Palabras clave|SOA, Servicios, Sistemas, Aplicaciones, Dependencia, Niveles de uso|
|Autor||
|Fuente||
|Secuencia|Padre [N003e. Catálogo de Servicios FNA-1](N003e.%20Catálogo%20de%20Servicios%20FNA-1.md)|
|Vínculos||

<br>

## Servicios SOA y Aplicaciones Proveedoras/Consumidoras
Las aplicaciones proveedoras de servicios SOA más significativas, según la cantidad de servicios provistos, son las primeras cinco (5) de la lista siguiente, y son también las aplicaciones que deben entrar a consideración del gobierno de aplicaciones y del gobierno SOA del Fondo.

|**Aplicación propietaria o proveedora**|**Cantidad de Servicios**|
|-----------------------------------|---------------------|
|Sin Proveedor|44|
|Cobis-Clientes|**39**|
|AA003-COBIS Cesantias|**18**|
|AA005 - COBIS Cartera|**15**|
|AA015 - COBIS Clientes|**13**|
|AA002-COBIS Ahorro voluntario|9|
|IIB UT-BUS|5|
|AA001-COBIS Admin Seguridad|5|
|Cobis-Cesantias|4|
|AA006 - COBIS Trámites|4|
|Cobis-AVC|4|
|AA012 - COBIS Contabilidad|3|
|Gemalto|3|
|Solati-ADMINFO|3|
|AA033 - COBIS Caja y Bancos|3|
|AA032 - Autenticación Externa|2|
|AA014 - COBIS Cobranzas|1|
|WorkManager|1|
|UT - Central de Citas|1|
|AA002-COBIS Caja y Bancos|1|
|AA072 - WSUtilitario|1|
|Vigia|1|
|AA080-WSFramework|1|
|AA016-COBIS Garantias|1|
|AA081-Comunicados|1|
|AA017 - COBIS Presupuesto|1|
|Cobis-Cartera|1|
|AA038-COBIS Admin Referencias|1|

_Fuente: Portafolio Unificado Servvicios FNA 0.0.1.xlsx_

<br>

En el Anexo 1 está el detalle de los servicios relacionados con la aplicación Cobis-Clientes que tomamos como ejemplo.

<br>

### Atención
Las siguientes servicios no tienen catalogada una aplicación proveedora, y por tanto, pueden ser ignoradas por las acciones de gestión o evolución que los requieran.

|**Servicio**|**Aplicación/proveedor**|
|------------|------------------------|
|Cesantias\_EliminarSolicitudRetiro|Sin Proveedor|
|Cesantias\_ModificarSolicitudRetiro|Sin Proveedor|
|Cesantias\_CrearSolicitudRetiro|Sin Proveedor|
|Credito\_RecuperarDetalleTramiteCredito|Sin Proveedor|
|Credito\_GenerarCertificado|Sin Proveedor|
|Csntias\_GenerarCertificacionSaldos|Sin Proveedor|
|Crdto\_GenerarCertificacionIntereses|Sin Proveedor|
|CntaAVC\_GenerarCertificacion|Sin Proveedor|
|Participante\_ValidarListasInhibitorias|Sin Proveedor|
|Credito\_RecuperarFlujoTramiteSolicitud|Sin Proveedor|
|Credito\_RecuperarDetalleTramiteSolicitud|Sin Proveedor|
|BProyectos\_ModificarProyecto|Sin Proveedor|
|BProyectos\_ModificarEstructura|Sin Proveedor|
|CuadroVentas\_VldarPgoPrrta|Sin Proveedor|
|Prtcpnte\_RcprarInfoIdCntralRsgo|Sin Proveedor|
|Prtcpnte\_EvluarCstnrioCnfrnta|Sin Proveedor|
|Prtcpnte\_RcprarCstnrioCnfrnta|Sin Proveedor|
|PQYR\_Rgstrar|Sin Proveedor|
|Grntias\_RcprarDtosBscos|Sin Proveedor|
|Csntias\_MdfcarMPC|Sin Proveedor|
|Csntias\_CnclarMPC|Sin Proveedor|
|Csntias\_RgstrarMPC|Sin Proveedor|
|Csntias\_RcprarInfoMPC|Sin Proveedor|
|CuentaAVC\_RecuperarDatosBasicos|Sin Proveedor|
|CuentaAVC\_RecuperarMovimientos|Sin Proveedor|
|Cesantias\_RecuperarDetalleTramiteRetiro|Sin Proveedor|
|Cesantias\_RecuperarTramitesRetiro|Sin Proveedor|
|Cesantias\_RecuperarMovimientos|Sin Proveedor|
|Libranza\_NotificarPagoPlanilla|Sin Proveedor|
|Libranza\_RecuperarDatosPlanillaPago|Sin Proveedor|
|Contabilidad\_CrearTerceroContable|Sin Proveedor|
|Tesoreria\_GenerarOrdenPago|Sin Proveedor|
|Presupuesto\_RecuperarDatosBasicosCDP|Sin Proveedor|
|Contabilidad\_RecuperarDatosCentroCosto|Sin Proveedor|
|Contabilidad\_RecuperarDatosCuentaContable|Sin Proveedor|
|Credito\_ModificarInformacionCobroJuridicoEnCobis|Sin Proveedor|
|Credito\_InformarCambioEstadoEtapaCobroJurídico|Sin Proveedor|
|BProyectos\_CrearEstructura|Sin Proveedor|
|CuadroVentas\_CrearSolicitud|Sin Proveedor|
|CrearProyectoInmobiliarioRequest|Sin Proveedor|
|Credito\_RecuperarTablaAmortizacion|Sin Proveedor|

_Fuente: Portafolio Unificado Servvicios FNA 0.0.1.xlsx_

<br>

## Servicios y Aplicaciones del FNA con Mayor Grado de Dependencia (potencial impacto)
El nivel de relación de dependencia de las aplicaciones con los servicios FNA da cuentas del esfuerzo de mantenimiento al momento de hacerles a estas cambios correctivos o evolutivos. La alta dependencia también tiene implicaciones en la flexibilidad al momento de dar una respuesta mediante los servicios SOA a las aplicaciones o procesos que los usan.

|**Componente o Aplicación**|**Dependencia Servicios**|
|---------------------------|-------------------------|
|Cobis|**78**|
|COBIS - Clientes|**30**|
|ProxyBizagi|**29**|
|COBIS - Crédito|**29**|
|Aplicación Ext - Banlínea|20|
|Aplicación Back - Bizagi Engine|20|
|Aplicación Web - Scoring|12|
|SafeNet BSIDCA|11|
|WM\_APIv2|10|
|...||
|**Total general**|**328**|

[Tabla. ]() Nivel de dependencia aplicaciones del FNA a de servicios SOA.

_Fuente principal: elaboración propia. **Fuente secundaria**: ae_fna_as_is.archimate, arquitectura fna.archimate_

<br>

>**Nota**. Las aplicaciones y los servicios SOA implicados en los niveles de dependencia superiores a 10 relaciones deben ser sujeto de gobierno SOA.

<br>

## Servicios del Portafolio con Mayor Grado de Uso (potencial impacto)
Los servicios SOA objeto de esta consultoría del portafolio SOA del Fondo que acumularn la mayor referencias de aplicaciones FNA, y por tanto, son causa de dependencia, son los marcados en el extracto siguiente. Para hacer foco en lo importante, la lista contiene únicamente servicios con más de 5 relaciones de uso (están siendo usados por otro sistema).

Los servicios SOA con mayor cantidad de relaciones (tienen o causan dependencia) organizados por aplicacioón proveedora.

|**Aplicación Proveedora**|**Servicios**|**Cantidad de Usos**|
|-------------------------|-------------|--------------------------|
|**COBIS**|AS055-ConsultaConsumidorFinanciero|**12**|
||AS150-ModificacionFormularioTramiteCredito|**11**|
||AS093-ModificaciónTramiteCredito|**9**|
||AS026-Gestión de Autenticación|8|
||AS149-CreacionTramiteCredito|6|
||AS163-GeneracionFormularioAfiliacionCesantias|6|
||AS038-ConsultaCuentaAVC|6|
||AS144-CreacionRelacionCliente|6|
||AS049-ConsultaTramiteCredito|6|
||AS034-consultarestadocuentaCartera|6|
||AS050-ConsultaPuntajeCredito|6|
||AS033-ConsultaProductosConsumidorFinanciero|6|
||AS068-ModificacionConsumidorFinanciero|6|
||AS164-GeneracionFormularioAfiliacionCesantias\*|5|
||ASXX3-registrarRecaudoObligacion|5|
||AS079-GeneracionExtractoCuentaCesantias|5|
||...||
|**ESB**|ESB\_001\_ClientePN\_RecuperarProductos|**14**|
||ESB\_133\_Credito\_NotificarEstadoDesembolso|**14**|
||ESB\_024\_ClientePN\_RecuperarInformacionBasica|**12**|
||ESB\_190\_GestorDocumental\_ConsultarDocumento|11|
||ESB\_063\_Credito\_RecuperarDetalleTramite|11|
||ESB\_075\_Seguridad\_AdministrarConexion2FA - CQ148541|10|
||ESB\_097\_Credito\_RecuperarFlujoTramite|10|
||ESB\_106\_Credito\_EnrutarTramiteCredito|9|
||ESB\_022\_Credito\_RecuperarTramiteSolicitudes|8|
||ESB\_204\_Credito\_CalcularPuntajeOrq|8|
||ESB\_194\_GestorDocumental\_ObtenerInformacionFormulario|8|
||ESB\_033\_CuentaAVC\_ConsultarCuenta|8|
||ESB\_022\_Credito\_RecuperarTramiteSolicitudes - CQ90537|7|
||ESB\_121\_Cesantias\_EncapsulaEliminacion - WI3992|7|
||ESB\_178\_ClientePJ\_ConsultaInfoEmpresarial|7|
||ESB\_163\_Cesantias\_GenerarFormularioAfiliacion|7|
||ESB\_207\_Credito\_ConsultarPuntaje|7|
||ESB\_079\_ClientePersonaJuridica\_CreacionRapidaPersonaJuridica|6|
||...|
|**Process Server**|AS020 - GestorConsultasCRED|6|
||**Total general (incluye todas las relaciones)**|**749**|

_Fuente: Portafolio Unificado Servvicios FNA 0.0.1.xlsx_

<br>

### Diagrama de Interdependencias del Portafolio FNA (niveles de acoplamiento)
El diagrama muestra la misma información que la tabla de dependencias del portfolio del FNA aunque expone mejor las interrelaciones entre servicios SOA pertenecesintes a las tres (3) aplicaciones citadas en el diagnóstico: Cobis, ESB y Process Server. También se puede apreciar mejor el peso tiene el concepto de las dependencias para el Fondo. Las áreas con mayor concentración de dependencias son aquellas que acumulan más líneas salientes.

<br>

    (arriba, izq.) Grupo de aplicaciones pertenecientes a Cobis. (centro, izq.) Grupo de aplicaciones que pertenecen al Process Server del Fondo. (abajo, izq.) El grupo de aplicaciones ESB IBM de la empresa.

![][embedView]

[Imagen. ]() Interdependencias del Portafolio FNA.

_Fuente: Portafolio Unificado Servvicios FNA 0.0.1.xlsx_

<br>

### Atención
No hay información para determinar el rol de cada relación entre los grupos de servicios: servicios de Cobis, servicios de Process Server y servicios del ESB. Esto es importante porque no conocemos si los servicios del bus son intermediarios, orquestadores o controladores: si por cada servicio SOA el bus replica estos, las replicas tendría el rol de intermediario; en cambio, si el bus organiza o secuencia a los otros servicios, estos servicios organizadores tendrían el rol de orquestador. 

<br>

## Anexo 1. Servicios Relacionados con (aplicación) Cobis-Clientes
Los 39 servicios SOA asociados con la aplicación Cobis-Clientes son los siguientes.

|**Servicio**|**Aplicación/proveedor**|
|------------|------------------------|
|Seguridad\_ValidarIdentidadBiometria|Cobis-Clientes|
|ClntePrsnaJrdca\_RecuperarInfoRapidaPJ|Cobis-Clientes|
|ClntePrsnaNtral\_RecuperarInfoBasica\_V2|Cobis-Clientes|
|ClntePrsnaJrdca\_CreacionRapidaPJ|Cobis-Clientes|
|ClntePrsnaNtral\_CreacionRapidaPN|Cobis-Clientes|
|ClntePrsnaNtral\_RecuperarNumerosProducto|Cobis-Clientes|
|ClntePrsnaJrdca\_RecuperarInfoFinancieraV2|Cobis-Clientes|
|ClntePrsnaJrdca\_RecuperarInfoLegalV2|Cobis-Clientes|
|ClntePrsnaJrdca\_RecuperarInfoBasicaV2|Cobis-Clientes|
|ClntePrsnaJrdca\_ModificarCasillaPostal|Cobis-Clientes|
|ClntePrsnaJrdca\_ModificarReferencias|Cobis-Clientes|
|ClntePrsnaJrdca\_ModificarInfoLegal|Cobis-Clientes|
|ClntePrsnaJrdca\_ModificarInfoBasica|Cobis-Clientes|
|ClntePrsnaJrdca\_CnsltrIfoCnsld|Cobis-Clientes|
|ClntePrsnaNtral\_MdfcarCsllPstl|Cobis-Clientes|
|ClntePrsnaNtral\_MdfcarInfoLbral|Cobis-Clientes|
|ClntePrsnaNtral\_MdfcarInfoFmliar|Cobis-Clientes|
|ClntePrsnaNtral\_MdfcarInfoBsca|Cobis-Clientes|
|Participante\_GenerarOperacionRios|Cobis-Clientes|
|Participante\_CrearOperacionRios|Cobis-Clientes|
|ClntePrsnaNtral\_GestionarCredenciales|Cobis-Clientes|
|ClntePrsnaJrdca\_MdfcarInfo|Cobis-Clientes|
|ClntePrsnaJrdca\_MdfcarInfo|Cobis-Clientes|
|ClntePrsnaNtral\_Crear|Cobis-Clientes|
|ClntePrsnaNtral\_Crear|Cobis-Clientes|
|ClntePrsnaJrdca\_Crear|Cobis-Clientes|
|ClntePrsnaJrdca\_Crear|Cobis-Clientes|
|ClntePrsnaNtral\_RcprarInfoLbral|Cobis-Clientes|
|ClntePrsnaNtral\_RcprarInfoLbral|Cobis-Clientes|
|ClntePrsnaNtral\_RcprarInfoFnncra|Cobis-Clientes|
|ClntePrsnaNtral\_RcprarInfoFnncra|Cobis-Clientes|
|ClientePersonaNatural\_RecuperarInformacion|Cobis-Clientes|
|ClientePersonaNatural\_RecuperarInformacion|Cobis-Clientes|
|ClientePersonaJuridica\_RecuperarInformacionLegal|Cobis-Clientes|
|ClientePersonaJuridica\_RecuperarDatosFinancieros|Cobis-Clientes|
|ClientePersonaJuridica\_RcprarDatosBasicos|Cobis-Clientes|
|ClientePersonaJuridica\_RecuperarInformacion|Cobis-Clientes|
|Cliente\_ValidarExistencia|Cobis-Clientes|
|ClntePrsnaNtral\_RecuperarProductos|Cobis-Clientes|

---
[embedView]:VistaPortafolio-CatalogoServiciosFNA.1.png


|Tema|Catálogo de Servicios: **Tipos de Servicios y Distribución de Servicios SOA por Tipo**
|----|-------------------------------------------------|
|Palabras clave|SOA, Servicios, Distribución de servicios|
|Autor||
|Fuente||
|Versión||
|Secuencia|Padre<br>Hijo||Vínculos||

<br>

## Catalogación de los Tipos de Servicios del Portafolio SOA, FNA

De la clasificación de servicios que dimos en la vista de contexto (servicios de información, proceso y negocio), y filtrando los servicios únicamente a los objeto de esta consultoría (vista de segmento), tenemos que la mayor cantidad de servicios del portafolio son de información. 

La tabla siguiente muestra la población de servicios del portafolio FNA.

|||
|---------------|--|
|**Tipo Servicio**|**Cantidad**|
|Servicio Información|**55**|
|Servicio Proceso|18|
|Servicio Negocio|14|
|**Total general**|**87**|

[Tabla.]() Catalogación de los tipos de servicios SOA del FNA.

_Fuente: elaboración propia, FNA_PortafolioServiciosFinal+ConsumidoresyProveedores.xlsx_

<br>

    Lo anterior responde a que la mayor cantidad de servicios SOA que son relevantes para el Fondo sirven para transportar información, esto es, para responder a solicitudes de información de los procesos o aplicaciones. Así mismo, este grupo influye en la cantidad de esfuerzo en mantenimiento y gobierno SOA. Los servicios de negocio, aquellos que elaboran una respuesta mediante un cómputo (sea cálculo, diferencia, comparación...), y por tanto, inciden en la flexibilidad de negocio, son los de menor presencia en el portafolio FNA.

<br>


**Es importante** tener esta población presente porque puede estar influyendo en inclinar los esfuerzos hacia el mantenimiento de servicios de información, en lugar de a la velocidad de salida (tiempo de mercado) de las funcionalidades de negocio.

<br>

### Lista de Detalle de los Servicios de Proceso
Presentamos a continuación el detalle de una de las catalogaciones presentadas en la tabla anterior: los servicios de proceso.

|**Nombre Servicio**|**Proveedor**|**Consumidor**|**Tipo Servicio**|
|-------------------|-------------|--------------|-----------------|
|VS\_ESB\_2.0.0\_Credito\_RecuperarTramiteSolicitudes|COBIS AS058|COBRANZA|Servicio Negocio|
|VS-ESB-1.3.0-Cesantias-CrearSolicitudRetiro|Cobis|APP MOVIL|Servicio Negocio|
|VS-ESB-1.1.0-CuentaAVC-CrearSolicitudRetiro|Cobis|APP MOVIL|Servicio Negocio|
|VS-ESB-1.0.0-CuentaAVC-ConsultarScoring|Cobis|Aplicaciones FNA|Servicio Negocio|
|VS\_ESB\_1.0.0\_CuentaAVC\_GestionCuentaAVC|Cobis|APP MOVIL|Servicio Negocio|
|VS\_ESB\_1.0.0\_Credito\_RechazarTramiteCredito|Cobis|bizagi|Servicio Negocio|
|VS\_ESB\_1.0.0\_Credito\_GenerarCertificadoService|Cobis|FONDO EN LINEA|Servicio Negocio|
|VS\_ESB\_1.0.0\_Credito\_EnrutarTramiteCredito|Cobis|bizagi|Servicio Negocio|
|VS\_ESB\_1.0.0\_Credito\_AsignarEstacionTramiteCredito|Cobis|ASESOR FNA|Servicio Negocio|
|VS\_ESB\_1.0.0\_Cesantias\_CrearSolicitudRetiro|Cobis|APP MOVIL|Servicio Negocio|
|VS-ESB-1.0.0-Credito-NotificarEstadoDesembolso|BIZAGI|COBIS|Servicio Negocio|
|VS\_ESB\_1.0.0\_CuadroVentas\_CrearSolicitud|ADMINFO|ATENCIÓN AL CLIENTE|Servicio Negocio|
|VS\_ESB\_1.0.0\_CuentaAVC\_CalcularPuntajeService|||Servicio Negocio|
|VS\_ESB\_1.0.0\_Credito\_InformarCambioEstadoEtapaCobroJuridico|||Servicio Negocio|


_Fuente: elaboración propia. Catalogo_FNA.xlsx_


|Tema|Catálogo de Servicios: **Procesos del FNA relacionados con los productos, objetivos, y áreas FNA objeto del diagnóstico SOA**
|----|-------------------------------------------------|
|Palabras clave|SOA, Servicios, Procesos|
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos||

<br>

## Procesos del FNA relacionados con Servicios del FNA Objeto del Diagnóstico SOA

A falta de información directa respecto de la relación de los procesos de negocio con los servicios, hacemos la propuesta mediante la relación de procesos y aplicaciones, _misma que sirve para inferir los servicios que están soportando a dichos procesos_. La vista siguiente muestra que falta la relación entre los procesos de negocio y los servicios hasta una profundidad de nivel 3. Vista de relación entre los procesos misionales del FNA y las aplicaciones que los soportan (los modelos no contienen la relación directa entre procesos y servicios SOA). _Lo que muestra la vista puede responder a una realidad probable en la que no hay relación explícita entre los procesos de negocio y los servicios_, y que por tanto, el Fondo tiene únicamente categorías de servicios utilitarios más que de procesos, o que los modelos simplemente no contienen estas relaciones.

![Imagen. ](VistaRelacionProcesosServicios.png)

<br>

La relación entre procesos y aplicaciones del Fondo siguiente nos da la pauta de que los que agrupan la mayor cantidad de servicios (aplicaciones) son el proceso de Facturación y Cartera (23 relaciones a aplicaciones), el proceso de Gestión de Crédito (19 relaciones a aplicaciones) y el de Gestión Comercial (19 relaciones a aplicaciones). Abajo visualizamos las relaciones de uno de los procesos para conocer la aplicaiones del FNA con las que este tiene relación.

|**Proceso**|**Relaciones**|
|-----------|----------------------------|
|Facturación y Cartera|**23**|
|Gestión de Crédito|**19**|
|_(en blanco)_|**19**|
|Gestión Comercial|9|
|Cesantías|5|
|Comunicación|3|
|Gestión Jurídica|3|
|Contrataciones|3|
|Gestión Administrativa|3|
|Gestion Comercial|3|
|Mercadeo|2|
|Aporte de Cesantías|2|
|Gestión Comercial, Comunicación|1|
|Gestion Humana|1|
|Captación de Ahorro Voluntario|1|
|**Total general**|**97**|

[Tabla.]() Procesos del FNA con mayor cantidad de relaciones a aplicaciones.

_Fuente: InventarioAplicacionesFNA.xlsx_

<br>

Para ejemplificar las relaciones de los procesos con las aplicaciones, tomaremos el proceso Facturación y Cartera para listar las aplicaciones implicadas con este.

|**Proceso**|**Aplicación**|**Canal**|
|-----------|--------------|---------|
|Facturación y Cartera|Abogados Externos|Internet|
|Facturación y Cartera|Adminfo cobranza|Oficina|
|Facturación y Cartera|Adminfo crédito|Oficina|
|Facturación y Cartera|Aplicación ASOCAJAS|Externo|
|Facturación y Cartera|Aplicación Banco de Bogotá|Externo|
|Facturación y Cartera|Aplicación Banco de Occidente|Externo|
|Facturación y Cartera|Aplicación Banco Sudameris|Externo|
|Facturación y Cartera|Aplicación Bancolombia|Externo|
|Facturación y Cartera|Aplicación Cadena|Oficina|
|Facturación y Cartera|Aplicación Colpatria|Externo|
|Facturación y Cartera|Aplicación Davivienda|Externo|
|Facturación y Cartera|Aplicación Helm|Externo|
|Facturación y Cartera|Aplicación Operador Aportes En Línea|Externo|
|Facturación y Cartera|Aplicación Operador Asopagos|Externo|
|Facturación y Cartera|Aplicación Operador Enlace Operativo|Externo|
|Facturación y Cartera|Aplicación Operador Mi Planilla|Externo|
|Facturación y Cartera|Aplicación Operador Simple|Externo|
|Facturación y Cartera|Aplicación Operador SOI|Externo|
|Facturación y Cartera|Aplicación SuRed|Externo|
|Facturación y Cartera|COBIS Cartera|Oficina|
|Facturación y Cartera|COBIS Garantías|Oficina|
|Facturación y Cartera|Contingencia Banco de la Republica|Oficina|
|Facturación y Cartera|Ecollect/Avisor/PSE|Internet|

[Tabla.]() Relaciones del proceso Facturación y Cartera del FNA.

_Fuente: InventarioAplicacionesFNA.xlsx_

<br>

### Atención
Las siguientes aplicaciones del Fondo no tienen relación con procesos, aparecen "en blanco" en la tabla anterior y en el modelo analizado: _InventarioAplicacionesFNA.xlsx_.

|**Aplicación**|**Proceso**|
|----------|-----------|
|IDM|Sin proceso|
|FINAC|Sin proceso|
|GoAnyWhere|Sin proceso|
|ERP SAP|Sin proceso|
|ASOCAJAS|Sin proceso|
|WorkManager|Sin proceso|
|Banlinea|Sin proceso|
|Autenticación IVR|Sin proceso|
|OASIS|Sin proceso|
|GHumana|Sin proceso|
|Fondo En Linea Personas|Sin proceso|
|Fondo En Linea Empresarial|Sin proceso|
|COBIS REC|Sin proceso|
|COBIS Admin Referencias|Sin proceso|
|COBIS VisualBatch|Sin proceso|
|COBIS Contabilidad|Sin proceso|
|COBIS Presupuesto|Sin proceso|
|COBIS Admin Seguridad|Sin proceso|
|Mi vivienda en linea / Vitrina virtual|Sin proceso|

[Tabla.]() Apliaciones del FNA sin relaciones con procesos.

_Fuente: InventarioAplicacionesFNA.xlsx_



## Descripción de la vista de Información actual

La vista funcional actual tiene como objetivo identificar el estado actual de los diferentes artefactos y la relación entre estos. Como lo son, los catálogos de entidades de datos y bases de datos; las matrices que permiten identificar las relaciones entre catálogos y los diagramas que ilustran las relaciones antes mencionadas.

## Marcos de Referencia

La arquitectura se construye teniendo en cuenta una serie de marcos de referencia como DAMA, el Marco de Referencia de Arquitectura Empresarial para el Estado Colombiano V2.0, TOGAF, entre otros. Estos marcos de referencia ayudan a la tener criterios para realizar un diagnóstico inicial, un nivel de madurez y la posterior construcción de un plan a futuro que debe ser implementado y que se guía por una hoja de ruta de iniciativas.

La Ilustración a continuación, muestra los marcos de referencia aplicables a la vista de Información:

![](vinformacion-marcos.jpg)
[Ilustracion 1.]() Marcos de referencia vista de Información

<br>

## Lista de Aplicaciones

A continuación, se listan las diferentes aplicaciones que hacen parte del ecosistema de integración de servicios del FNA:

| **Aplicación Destino** | **URL** | **Virtual Server** |
| --- | --- | --- |
| ECOLLECT | [https://aplicacionesweb.fna.gov.co:8090/eCollectERPAgent/](https://aplicacionesweb.fna.gov.co:8090/eCollectERPAgent/) | aplicacionesweb |
| ADMINFO | [https://ext.fna.gov.co:8090/CobroAdministrativo/](https://ext.fna.gov.co:8090/CobroAdministrativo/) | ext |
| TRANSUNION | [https://ext.fna.gov.co:8090/transunion/](https://ext.fna.gov.co:8090/transunion/) | ext |
| REGISTRADURIA NACIONAL | [https://ext.fna.gov.co:8090/RegistraduriaANI/](https://ext.fna.gov.co:8090/RegistraduriaANI/) | ext |
| CAMERFIRMA | [https://ext.fna.gov.co:8090/CorreoSeguro/](https://ext.fna.gov.co:8090/CorreoSeguro/) | ext |
| SAP | [https://fnabogsoa.fna.gov.co:8099/fna-poprd/](https://fnabogsoa.fna.gov.co:8099/fna-poprd/) | fnabogsoa |
| SECUREID | [https://ext.fna.gov.co:8090/api/consultas/](https://ext.fna.gov.co:8090/api/consultas/) | ext |
| MASIVIAN | [https://ext.fna.gov.co:8090/MasivianOTP/](https://ext.fna.gov.co:8090/MasivianOTP/) | ext |
| SFC | [https://ext.fna.gov.co:8090/SmartSupervision/](https://ext.fna.gov.co:8090/SmartSupervision/) | ext |
| COBIS | [https://fnabogsoa.fna.gov.co:8099/WSAdmin/](https://fnabogsoa.fna.gov.co:8099/WSAdmin/) | fnabogsoa |
| VIABILIDAD | [https://fnabogsoa.fna.gov.co:8099/viabilidad-api/](https://fnabogsoa.fna.gov.co:8099/viabilidad-api/) | fnabogsoa |
| ADMINCREDITO | [https://fnabogsoa.fna.gov.co:8099/admincredito-api/](https://fnabogsoa.fna.gov.co:8099/admincredito-api/) | fnabogsoa |
| CARGUEDOCUMENTOS | [https://fnabogsoa.fna.gov.co:8099/carguedocumentos-api/](https://fnabogsoa.fna.gov.co:8099/carguedocumentos-api/) | fnabogsoa |
| SIMULADOR | [https://fnabogsoa.fna.gov.co:8099/Simulador/](https://fnabogsoa.fna.gov.co:8099/Simulador/) | fnabogsoa |
| CONFECAMARA | [https://aplicacionesweb.fna.gov.co:8090/CamaraComercio/](https://aplicacionesweb.fna.gov.co:8090/CamaraComercio/) | aplicacionesweb |
| VIGIA | [https://aplicacionesweb.fna.gov.co:8090/vigia2/](https://aplicacionesweb.fna.gov.co:8090/vigia2/) | aplicacionesweb |
| WORKMANAGER | [https://fnabogsoa.fna.gov.co:8099/GestorDocumental/](https://fnabogsoa.fna.gov.co:8099/GestorDocumental/) | fnabogsoa |
| BIZAGI | [https://aplicacionesweb.fna.gov.co:8090/BizagiProxyServices/](https://aplicacionesweb.fna.gov.co:8090/BizagiProxyServices/) | aplicacionesweb |
| APP MOVIL | [http://172.16.127.116/FNA/Web/WJ\_verificarNotificacionesPush.aspx](http://172.16.127.116/FNA/Web/WJ_verificarNotificacionesPush.aspx) | aplicacionesweb |

_Tabla 1 Portafolio de Aplicaciones_

<br>

  ## Lista de Proveedores

A continuación, se listan los diferentes proveedores que hacen parte del ecosistema de integración de servicios del FNA:

| **Aplicación Destino** | **URL** | **Virtual Server** | **Contexto** |
| --- | --- | --- | --- |
| ADMINFO | [https://ext.fna.gov.co:8090/CobroAdministrativo/](https://ext.fna.gov.co:8090/CobroAdministrativo/) | ext | "/CobroAdministrativo/\*" |
| TRANSUNION | [https://ext.fna.gov.co:8090/transunion/](https://ext.fna.gov.co:8090/transunion/) | ext | "/transunion/" |
| REGISTRADURIA NACIONAL | [https://ext.fna.gov.co:8090/RegistraduriaANI/](https://ext.fna.gov.co:8090/RegistraduriaANI/) | ext | "/RegistraduriaANI/\*" |
| TRANSUNION | [https://ext.fna.gov.co:8090/transunion-dc/](https://ext.fna.gov.co:8090/transunion-dc/) | ext | "/transunion-dc/" |
| CAMERFIRMA | [https://ext.fna.gov.co:8090/CorreoSeguro/](https://ext.fna.gov.co:8090/CorreoSeguro/) | ext | "/CorreoSeguro/\*" |
| SECUREID | [https://ext.fna.gov.co:8090/api/consultas/](https://ext.fna.gov.co:8090/api/consultas/) | ext | "/api/consultas\*" |
| MASIVIAN | [https://ext.fna.gov.co:8090/MasivianOTP/](https://ext.fna.gov.co:8090/MasivianOTP/) | ext | "/MasivianOTP/\*" |
| SFC | [https://ext.fna.gov.co:8090/SmartSupervision/](https://ext.fna.gov.co:8090/SmartSupervision/) | ext | "/SmartSupervision/\*" |

_Tabla 2 Portafolio de Proveedores_

<br>

## Entidades de Datos

Las entidades son una encapsulación de datos que describen un objeto de relevancia para la operación del FNA. Las entidades de datos o información se pueden vincular a aplicaciones, repositorios y servicios que se pueden estructurar de acuerdo con las consideraciones de implementación específicas de sistemas y soluciones.

Para el alcance de la vista de información, se tuvo como fuente de información el modelamiento a nivel lógico, para identificar entidades de información a nivel conceptual de los archivos de la herramienta de modelamiento.

La tabla a continuación, muestra las entidades de datos identificadas y el número de servicios con los que tienen relación:

| **Entidades** | **Cantidad de servicios** |
| --- | --- |
| **Credito** | **50** |
| **Cesantias** | **45** |
| **CuentaAVC** | **30** |
| **ClientePN** | **23** |
| **Seguridad** | **17** |
| **Cartera** | **16** |
| **ClientePJ** | **14** |
| **GestorDocumental** | **14** |
| **Tesoreria** | **8** |
| **PQYR** | **6** |
| **Administrador** | **4** |
| **Clientes** | **3** |
| **Garantias** | **2** |

_Tabla 3 Entidades de Datos_

<br>

## Inventario de fuentes de datos (BD)

A continuación, se listan las fuentes de información que son usadas para ingestar o carga cargar datos desde o hacia el ecosistema de integración del FNA:

| **NOMBRE** | **RESPONSABLE** |
| --- | --- |
| **FNABOGPROD1**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGFLASH**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGIQPRO1**
 SAP ASE Platform Edition Plataforma 16 SP11
 SAP IQ nodo1 | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGIQPRO2**
 SAP ASE Platform Edition Plataforma 16 SP11
 SAP IQ nodo2 | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGIQPRO**
 CAPE | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPROD1**
 CAPE | SERVICIO BASE DE DATOS : Grupo Base de Datos FNA
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGRSPRO**
 SAP ASE Platform Edition Plataforma 16 SP11
 SAP IQ | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **fna-hanabipro**
 SAP HANA Enterprise Edition Plataforma 1.0 SP12 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPREP1**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **JUPASCANG05BEG01**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPREP1\_TSM**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPRUE**
 SAP Adaptive Server Platform 16.0 SP03 PL06 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGIQPRE**
 SAP ASE Platform Edition Plataforma 16 SP11
 SAP IQ | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGRSPRU**
 SAP ASE Platform Edition Plataforma 16 SP11
 SAP IQ | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **fna-hanabiqa**
 SAP HANA Enterprise Edition Plataforma 1.0 SP12 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGAPP008**
SAP Data Services 4.2 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPAPP005**
SAP Data Services 4.2 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGBOPRO**
SAP Business Objects Enterprise Premiun 4.2 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPBO**
SAP Business Objects Enterprise Premiun 4.2 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVPPWP018**
 Oracle Database 11g Release 11.2.0.4.0 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGBDOR01**
 Oracle Database 11g Release 11.2.0.4.0 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGGIT-01**
 Oracle Database 12c Standard Edition Release 12.1.0.2.0 - 64bit Production | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVPPWP023** \FVIRTUALCL2008
 SQL SERVER 2008 Microsoft SQL Server Enterprise Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCL01BD02** \MSSQL2008 SQL SERVER 2008 Microsoft SQL Server Enterprise Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD01WP002** \MSSQL2014 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD02WP002** \MSSQL2014\_2 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD03WP002** \APMSQL2014 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| BOGPVBD04WP002\SHAREPOINT
 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD05WP002** \SMSQL2014 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD01WP003** \WMSQL2016 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD02WP003** \MSSQL2016\_1 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBDWP013** \RSMSSQL2016 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCOV-03** \SA SQL SERVER 2012 Standard Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGDCL01N6** \CFVIRTUALCL2008 SQL SERVER 2008 Microsoft SQL Server Enterprise Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGDPCL01N1** \CMSSQL2008 SQL SERVER 2008 Microsoft SQL Server Enterprise Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGDCL01N5** \DMSSQL2008 SQL SERVER 2008 Microsoft SQL Server Enterprise Edition (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCCL02BD02** \PMSSQL2014
 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCCL02BD01** \CMSSQL2014
 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCCL02BD04** \DMSSQL2014 SQL SERVER 2014 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBD01WC002\** PMSSQL2016
 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCCL04BD02\PFVIRTUAL2016**
 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| BOGPVBD02WC002\CMSSQL2016 SQL SERVER 2016 Microsoft SQL Server Enterprise: Core-based Licensing (64-bit) | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **BOGPVBDWC007** \RSCMSSQL2016 SQL SERVER 2016 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGCDBAPP**
 DB2 Enterprise Server Edition 64 bits | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGDBAPP\_68**
 DB2 Enterprise Server Edition 64 bitsFNABOGDBAPP\_68 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGPDBAPP**
 DB2 Enterprise Server Edition 64 bits | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |
| **FNABOGSDBP**
 DB2 9.7.0.11 / 10.5.0.8 | SERVICIO BASE DE DATOS : Proveedor Encargado - Infraestructura
 SISTEMA OPERATIVO: Proveedor encargado - Infraestructura |

_Tabla 4 Inventario de Bases de Datos Activas_

La ilustración a continuación, muestra la vista de bases de datos y la infraestructura en la que están desplegadas:

![Ilustración 2 Vista de Bases de Datos](vinformacion-basesdedatos.png)
_Ilustración 2 Vista de Bases de Datos_

<br>

## Matriz de Entidades de Datos Vs Procesos Misionales

Esta matriz permite identificar la relación existente entre los procesos del FNA en el contexto del proyecto y las entidades de datos identificadas en el ecosistema:

| **Procesos Misionales /Entidades de Datos** | Proceso de Aportes de Cesantías | Administración de Cuentas y Pagos Cesantías | Procesos Gestión de crédito Constructor | Procesos Gestión de Crédito Educativo | Procesos Gestión de Crédito Hipotecario |
| --- | --- | --- | --- | --- | --- |
| Credito |   |   | **x** | **x** | **x** |
| Cesantias | **x** | **x** |   |   |   |
| CuentaAVC | **x** | **x** |   |   |   |
| ClientePN | **x** | **x** | **x** | **x** | **x** |
| Seguridad | **x** | **x** | **x** | **x** | **x** |
| Cartera |   | **x** | **x** | **x** | **x** |
| ClientePJ | **x** | **x** | **x** | **x** | **x** |
| GestorDocumental | **x** | **x** | **x** | **x** | **x** |
| Tesoreria | **x** | **x** | **x** | **x** | **x** |
| PQYR | **x** | **x** | **x** | **x** | **x** |
| Administrador | **x** | **x** | **x** | **x** | **x** |
| Clientes | **x** | **x** | **x** | **x** | **x** |
| Garantias | **x** | **x** | **x** | **x** | **x** |

_Tabla 5 Matriz de Entidades de Datos VS Procesos Misionales_

<br>

## Observaciones

A continuación, se listan observaciones realizadas en este diagnóstico inicial:

- Si bien existen modelos de datos y diccionarios de las bases de datos más importantes como, por ejemplo: CORBIS, no se encontró un modelo de datos canónico que permita un lenguaje común en todos los modelos de datos, un entendimiento a toda la organización (técnico y funcional) y facilite la explotación y toma de decisiones a partir de los datos.
- Se evidencia que existe cierta desactualización en los artefactos que conforman la arquitectura de datos. (Modelo de datos empresarial, diccionario de datos, catálogos, matrices y diagramas).
- Existen diccionarios de datos particulares para algunas bases de datos, aunque se requiere un diccionario de datos de forma estandarizada, que permita facilitar el entendimiento de éstos y sus relaciones. Así como diccionarios de otro tipo de datos: maestros y referencias, analíticos, transaccionales y de metadatos.
- Aunque existen algunas actividades realizadas en torno al gobierno de datos, que incluso fue propuesto como iniciativa en el PETI con fecha a 2022, es necesario retomar este proyecto que permita al FNA tener una gestión de los datos más apropiada mediante la incorporación de lineamientos, directrices, indicadores en torno al gobierno de los datos
- Se tienen identificados los dominios de información, aunque es importante aterrizar cuales de estos son datos maestros y referencias mediante un levantamiento tanto funcional como técnico de estos. Y que permitan a través de una estrategia, tener una vista unificada de los datos que conlleven a la democratización y uso correcto de estos.
- Aunque se tienen desarrollos in house y el FNA es dueño de estos procesos, se presentan algunas necesidades en torno al ciclo de vida de los datos donde se ve la obligación de recurrir a los proveedores. Anterior, genera una alta dependencia para el desarrollo de actividades operativas (inclusión de campos, reglas de negocio, generación de indicadores, entre otras).

## Fuentes de Información

- The Enterprise Data Model: a framework for enterprise data architecture, 2nd Edition. (2012, mayo 7). Andy Graham.
- DAMA-DMBOK: Data Management Body of Knowledge, 2nd Edition. (2017, Julio 5). Dama International.


|Tema|Descripción de la vista de integración actual: **Matriz de intercambio de información crítica del negocio**
|----|-------------------------------------------------|
|Palabras clave|SOA, Integración, EAI, Punto a punto|
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos|[N005a. Vista de Integración FNA-2](N005a.%20Vista%20de%20Integración%20FNA-2.md)|

<br>

## Matriz de Intercambio de Información Crítica del Negocio
La integraciones FNA las entendemos como interacción punto a punto, o integración directa, sin mediación. Aunque son conocidas las ventajas de las integraciones punto a punto, es preferible mantenerlas en cantidades manejables.

La siguiente lista muestra la cantidad de integraiones del FNA y los cuidados que hay que tener tanto en las cantidades de integraciones punto a punto: _330 integraciones_, como con los casos de uso de integraciones no identificados: _273 integraciones sin caso_.

|**Caso de Integración**|**Integraciones**|
|-----------------------|-----------------|
|**(en blanco)**|**273**|
|CU0016 - Radicar solicitud de retiro AVC|11|
|CU0020 - Radicar solicitud de retiro de Cesantías|11|
|CU0006 - Radicar solicitud de retiro de cesantías|11|
|CU0002 - Radicar solicitud de retiro AVC|8|
|CU0018 - Enviar cartas de aprobación de crédito de una junta|3|
|CU0017 - Enviar carta de aprobación de crédito al consumidor financiero|3|
|CU0003 - Consultar solicitud de retiro AVC|2|
|CU0013 - Generar cartas de aprobación de crédito de una junta|1|
|CU0075 - Generar archivo de comprobantes contables titularizados|1|
|CU0071 - Generar archivo plano de órdenes de pago no procesadas por ERP|1|
|CU0072 - Procesar archivo de respuesta de órdenes pago por contingencia ERP|1|
|CU0014 - Consultar trámites de crédito de consumidor financiero|1|
|CU0004 - Eliminar solicitud de retiro AVC|1|
|CU0015 - Consultar detalle de trámite de crédito de consumidor financiero|1|
|CU0016 - Generar carta de aprobación de crédito|1|
|**Total general**|**330**|

[Tabla. ]() Integraciones del FNA. Caso de Integración

_Fuente: pt-inge-028-inventariointegraciones_v1.0.xlsx_

<br>

**Nota**: Las integraciones sin clasificación de casos de uso deben ser objeto de gobierno SOA. Sin conocer lo que estas integraciones transportan u operan, no es posible determinar redundancias negativas, en cuyo caso impactarían a la flexibilidad y a los costos de mantenimiento.

<br>

### Descripción de las Integraciones FNA
Las integraciones (más de 300, mostradas en la tabla de integraciones anterior) del FNA están descritas en términos de las aplicaciones que las usan. De acuerdo con esto, tenemos los dos extremos de cada integración. La primera tabla muestra las integraciones de las aplicaciones cuanto estas son el origen de la integración, mientras que la segunda tabla muestra las aplicaciones cuando son el destino.

Basado en lo anterior, las integraciones del FNA están descritas de la siguiente manera.
|**Aplicación Origen**|**Integraciones Salientes**|
|---------------------|---------------------------|
|AA074 - Fondo En Línea Personal|**60**|
|AA006 - COBIS Trámites|**33**|
|AA085 - Aplicación Movil CX|**27**|
|AA071 - Kioscos|**22**|
|AA002 - COBIS Ahorro Voluntario|**20**|
|AA003 - COBIS Cesantias|14|
|AA005 - COBIS Cartera|14|
|AA021 - Fondo En Línea|13|
|AA015 - COBIS Clientes|13|
|AA010 - COBIS Caja y Bancos Operativo|13|
|AA083 - CRM Salesforce|9|
|AA084 - ERP SAP|9|
|AA059 - Aplicación GEL|7|
|AA011 - Visual Batch|7|
|AA013 - COBIS Entidades|7|
|AA020 - Banca Virtual|6|
|AA012 - COBIS Contabilidad|5|
|...||
|**Total general**|**330**|

[Tabla. ]() Integraciones del FNA. Aplicaciones origen de la integración.

_Fuente: pt-inge-028-inventariointegraciones_v1.0.xlsx_

<br>

>Resaltamos los casos de las integraciones salientes mayores a 20, las cuales, por su nivel de interdependencia requieren de mayor gobierno SOA. No evidenciamos que exista gobierno SOA para controlar la población de las integraciones por aplicación o migrarlas a servicios SOA.

<br>

El anexo 1 incluido abajo es una muestra del detalle de las integraciones salientes de estas aplicaciones.

<br>

|**Aplicación Destino**|**Integraciones Entrantes**|
|----------------------|---------------------------|
|AA003 - COBIS Cesantias|**51**|
|AA002 - COBIS Ahorro Voluntario|**40**|
|AA015 - COBIS Clientes|**30**|
|AA038 - COBIS Admin Referencias|**25**|
|AA005 - COBIS Cartera|**24**|
|AA012 - COBIS Contabilidad|**22**|
|AA006 - COBIS Trámites|17|
|AA010 - COBIS Caja y Bancos Operativo|12|
|AA082 - Identificación Biométrica|11|
|AA084 - ERP SAP|10|
|AA017 - COBIS Presupuesto|9|
|AA069 - CONFRONTA|8|
|AA045 - Adminfo Cobro Juridico|8|
|AA097 - Signal Andes|8|
|AA070 - WorkManager|6|
|AA013 - COBIS Entidades|6|
|AA021 - Fondo En Línea|5|
|...||
|**Total general**|**330**|

[Tabla. ]() Integraciones del FNA. Aplicaciones destino de la integración.

_Fuente: pt-inge-028-inventariointegraciones_v1.0.xlsx_

<br>

>De igual manera, resaltamos los casos de las integraciones, en este caso entrantes,  mayores a 20. **Es importante** que estos casos sean discutidos por los miembros del gobierno SOA.

<br>

El anexo 2, abajo, es una muestra del detalle de las integraciones entrantes de estas aplicaciones.

<br>

### Clasificación de Aplicaciones por Integracion
Otro ejercicio de clasificación de las integraciones de FNA es por el rol de las aplicaciones participantes en cada integración: pueden ser _consumidoras o proveedoras_ de datos. Esta es una visión más práctica y afin a las posibles acciones que el Fondo puede tomar para organizar más las integraciones analizadas.

<br>

|**Aplicación Consumidora**|**Nivel Consumo**|
|--------------------------|-----------------|
|BUS|**15**|
|SF,CRM|**8**|
|Móviles|7|
|IVR,(37)|7|
|CX|6|
|ADMINFO|3|
|PQYR,(41)|3|
|Kactus,(44)|2|
|Atención,Cli|2|
|Libranza|2|
|CuadroVentas|2|
|Asig,Claves|2|

[Tabla. ]() Clasificación de integraciones del FNA. Aplicación más consumidora: ESB de FNA.

_Fuente: Catalogo de integraciones 1.0.8.xlsx_

<br>

|**Aplicación Proveedora**|**Nivel de Participación**|
|-------------------------|--------------------------|
|Clientes,(015)|**21**|
|BUS|5|
|Cartera,(005)|5|
|Cuadro Ventas|4|
|Cifin|3|
|2FA|3|
|PQYR,(41)|2|
|ADMINFO|2|
|AVC,(002)|2|
|Cesantías,(003)|2|

[Tabla. ]() Clasificación de integraciones del FNA. Aplicación más proveedora: **Cobis Clientes**.

_Fuente: Catalogo de integraciones 1.0.8.xlsx_

<br>

>Basado en las tablas anteriores, aplicaciones consumidoras y proveedoras, las aplicacion o sistemas que deben entrar a gobierno SOA son el ESB de FNA y el módulo del ERP Cobis Clientes.

<br>


## Anexos
### Anexo 1. Muestra de Integraciones Salientes. Aplicación AA003 - COBIS Cesantias del FNA
|**Código**|**Aplicación Origen**|**Aplicación Destino**|
|----------|---------------------|----------------------|
|AI0232|AA003 - COBIS Cesantias|AA084 - ERP SAP|
|AI0178|AA003 - COBIS Cesantias|AA005 - COBIS Cartera|
|AI0177|AA003 - COBIS Cesantias|AA017 - COBIS Presupuesto|
|AI0176|AA003 - COBIS Cesantias|AA017 - COBIS Presupuesto|
|AI0175|AA003 - COBIS Cesantias|AA012 - COBIS Contabilidad|
|AI0174|AA003 - COBIS Cesantias|AA012 - COBIS Contabilidad|
|AI0173|AA003 - COBIS Cesantias|AA010 - COBIS Caja y Bancos Operativo|
|AI0172|AA003 - COBIS Cesantias|AA010 - COBIS Caja y Bancos Operativo|
|AI0171|AA003 - COBIS Cesantias|AA010 - COBIS Caja y Bancos Operativo|
|AI0169|AA003 - COBIS Cesantias|AA005 - COBIS Cartera|
|AI0139|AA003 - COBIS Cesantias|AA038 - COBIS Admin Referencias|
|AI0122|AA003 - COBIS Cesantias|AA012 - COBIS Contabilidad|
|AI0060|AA003 - COBIS Cesantias|AA082 - Identificación Biométrica|
|AI0055|AA003 - COBIS Cesantias|AA082 - Identificación Biométrica|


### Anexo 2. Muestra de Integraciones Entrantes. Aplicación AA003 - COBIS Cesantias del FNA
|**Código**|**Aplicación Origen**|**Aplicación Destino**|
|----------|---------------------|----------------------|
|AI0333|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0332|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0331|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0330|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0329|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0328|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0327|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0326|AA071 - Kioscos|AA003 - COBIS Cesantias|
|AI0322|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0321|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0320|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0319|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0318|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0317|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0316|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0314|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0310|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0309|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0308|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0307|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0306|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0305|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0304|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0303|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0250|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0249|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0248|AA085 - Aplicación Movil CX|AA003 - COBIS Cesantias|
|AI0241|AA084 - ERP SAP|AA003 - COBIS Cesantias|
|AI0035|AA059 - Aplicación GEL|AA003 - COBIS Cesantias|
|AI0036|AA059 - Aplicación GEL|AA003 - COBIS Cesantias|
|AI0037|AA059 - Aplicación GEL|AA003 - COBIS Cesantias|
|AI0038|AA059 - Aplicación GEL|AA003 - COBIS Cesantias|
|AI0239|AA084 - ERP SAP|AA003 - COBIS Cesantias|
|AI0218|AA015 - COBIS Clientes|AA003 - COBIS Cesantias|
|AI0212|AA013 - COBIS Entidades|AA003 - COBIS Cesantias|
|AI0042|AA060 - Aplicación WAP|AA003 - COBIS Cesantias|
|AI0203|AA010 - COBIS Caja y Bancos Operativo|AA003 - COBIS Cesantias|
|AI0202|AA010 - COBIS Caja y Bancos Operativo|AA003 - COBIS Cesantias|
|AI0187|AA006 - COBIS Trámites|AA003 - COBIS Cesantias|
|AI0170|AA006 - COBIS Trámites|AA003 - COBIS Cesantias|
|AI0095|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0093|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0092|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0091|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0090|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0089|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0088|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0087|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0085|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0084|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|
|AI0082|AA074 - Fondo En Línea Personal|AA003 - COBIS Cesantias|


|Tema|Descripción de la vista de integración actual: **Entidades de negocio (información y datos) relacionadas en la integración**
|----|-------------------------------------------------|
|Palabras clave|SOA, Integración, Entidades de datos|
|Autor||
|Fuente||
|Secuencia|Padre<br>Hijo|
|Vínculos|[N005a. Vista de Integración FNA-1](N005a.%20Vista%2de%2Integracion%2FNA-1.md)|

<br>

## Entidades de Negocio (información y datos) Relacionadas
Si bien existe información sobre las entidades de datos de negocio del FNA, los modelos de integración de FNA no permiten encontrar la relación entre las operaciones punto a punto y los datos que transportan, sean resultado de operaciones, o entidades.

En la siguiente tabla presentamos una inferencia posible relación entre las integraciones punto a punto y las entidades canónicas de datos de FNA.

|**Entidad**|**Nivel de Uso**|
|-----------|:--------------:|
|archivo.xsd|**x**|
|aseguramientoProducto.xsd||
|asesor.xsd||
|autorizacionEnvio.xsd||
|beneficiario.xsd||
|bloqueo.xsd||
|casaCobranza.xsd||
|catalogos.xsd||
|cdp.xsd||
|centrocostos.xsd||
|cesantias.xsd|**x**|
|clasificacionInmueble.xsd||
|clasificacionParqueo.xsd||
|cliente.xsd||
|cobranza.xsd||
|cobrojuridico.xsd||
|codeudor.xsd||
|codigoTipo.xsd||
|composicionAreas.xsd||
|composicionGeneralInmobiliario.xsd||
|composicionNiveles.xsd||
|composicionParqueaderos.xsd||
|composicionSegmentosUnidades.xsd||
|composicionTiposUnidades.xsd||
|conceptoContable.xsd||
|consultacentrocostos.xsd||
|conversionUvr.xsd||
|credenciales.xsd||
|credito.xsd||
|cuentaAVC.xsd||
|cuentaBancaria.xsd||
|cuentacontable.xsd||
|cuentaproductocliente.xsd||
|cuentaproductocredito.xsd||
|cuotaCredito.xsd||
|cuotasMora.xsd||
|DatosRegistroInhibitorias.xsd||
|definicionEstructura.xsd||
|definicionProyecto.xsd||
|descuentoConceptoPago.xsd||
|descuentos.xsd||
|desembolso.xsd||
|destinacionAreas.xsd||
|detalleAreaConstruccion.xsd||
|detalleAreaLote.xsd||
|direccion.xsd||
|embargo.xsd||
|estadoEspecial.xsd||
|estructuras.xsd||
|excepciongenerica.xsd||
|funcionario.xsd||
|garantia.xsd||
|identificacion.xsd||
|infoCentralRiesgo.xsd||
|informacionCuentaMora.xsd||
|informacionEstructuraInmobiliaria.xsd||
|informacionfinanciera.xsd||
|informacionlaboral.xsd||
|informacionProyectoInmobiliario.xsd||
|inventarioViviendas.xsd||
|libranza.xsd||
|listasNegras.xsd||
|monedaExtranjera.xsd||
|niveles.xsd||
|ordenPago.xsd||
|paginacion.xsd||
|pagosCredito.xsd||
|pagosDeuda.xsd||
|participante.xsd||
|pep.xsd||
|personajuridica.xsd||
|personanatural.xsd||
|pignoracion.xsd||
|pqyr.xsd||
|proceso.xsd||
|productocliente.xsd||
|proyectos.xsd||
|relacion.xsd||
|reporteInhibitorias.xsd||
|resumenValorAPagar.xsd||
|saldodeudacredito.xsd||
|solicitud.xsd||
|telefono.xsd||
|tercero.xsd||
|tipoafiliacion.xsd||
|tramite.xsd||
|ubicacionOficinaProducto.xsd||
|ubicacionProyecto.xsd||

[Tabla. ]() Nivel de uso de las entidades canónicas en integraciones FNA

_Fuente: Inventario Canonico V1.0.0.xlsx_

<br>

**Nota**: según los modelos del repositorio FNA, el nivel de uso de las entidades canónicas es muy bajo. De igual manera que en el caso anterior, sin información de lo que estas integraciones transportan u operan, no es posible determinar redundancias negativas, en cuyo caso impactarían a la flexibilidad y a los costos de mantenimiento.

<br>

### Clasificación de Entidades por Áreas Propietaria
La relación de entidades de datos y áreas de negocio del FNA nos debe dar una idea de qué áreas se encuentran más estandarizadas en su comunicación con otros actores. La lista siguiente indica que el área de negocio más intensa en el uso de entidades de datos, y por tanto, la más estándar en su comunicación con otras _es el área de Crédito del FNA_.


|**Etiquetas de fila**|**Cuenta de Unidad Negocio**|
|---------------------|----------------------------|
|**Sin Unidad**|**60**|
|Crédito|**7**|
|Cartera|5|
|Clientes|4|
|Contabilidad|3|
|Inmueble|2|
|Jurídico|2|
|Cobranza|2|
|Garantía|1|
|Cesantía|1|
|Cuenta AVC|1|
|**Total general**|**88**|

[Tabla. ]() Nivel de uso de las entidades canónicas en integraciones FNA

_Fuente: elaboración propia_

<br>

>La lista anterior advierte además que la mayoría de entidades de datos canónicas no son atribuíbles a un área o proceso de negocio. Los modelos del FNA no evidencian esta relación, que es importante para conocer el nivel de estandarización en el uso del lenguaje canónico de intercambio de información.

<br>

La falta de relación entre las entidades y las áreas puede implicar la falta de un modelo de uso y gobierno de datos, de interoperabilidad, y de integración SOA mediante los que se pueda determinar por qué estas entidades son la únicas o se requieren más. En los documentos de repositorio SOA del FNA no hay evidencias de dichos modelos.

<br>

