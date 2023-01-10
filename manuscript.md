---
title: Manuscript Title
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2023-01-10'
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
  <meta name="dc.date" content="2023-01-10" />
  <meta name="citation_publication_date" content="2023-01-10" />
  <meta property="article:published_time" content="2023-01-10" />
  <meta name="dc.modified" content="2023-01-10T19:48:36+00:00" />
  <meta property="article:modified_time" content="2023-01-10T19:48:36+00:00" />
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
  <link rel="alternate" type="text/html" href="https://hwong23.github.io/fna-devdoc-f1-1/v/49f97830e57472875d4bc6b254ec8b91d1874409/" />
  <meta name="manubot_html_url_versioned" content="https://hwong23.github.io/fna-devdoc-f1-1/v/49f97830e57472875d4bc6b254ec8b91d1874409/" />
  <meta name="manubot_pdf_url_versioned" content="https://hwong23.github.io/fna-devdoc-f1-1/v/49f97830e57472875d4bc6b254ec8b91d1874409/manuscript.pdf" />
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

