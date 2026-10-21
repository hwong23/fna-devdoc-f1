Implementar el Sistema Documental de Arquitectura (SDA) desde un conjunto de plantillas CSV tal que genere una Wiki FNA orientada a arquitectura de solución e ingeniería, y que actúe como capa de conocimiento, navegación y gobierno. El SDA es el fundamento del repositorio de arquitectura FNA y está constituido por catálogos, matrices, modelos Archimate, gobierno, trazabilidad.

Adicionalmente, la documentación del SDA es articula con Azure Wikis como mecanismo colaborativo de documentación y búsqueda inicial de información y elementos de trabajo.


# Wiki del Sistema Documental de Arquitectura (SDA)
## Objetivo

Proveer una Wiki institucional que concentre el conocimiento arquitectónico del FNA y permita:

* Consultar arquitectura de los sistemas del FNA de forma sencilla.
* Mantener trazabilidad entre demanda, arquitectura, soluciones y operación.
* Integrar Archi, Azure Repos, Azure DevOps y el SDA (repositorio de arquitectura).
* Centralizar y servir como repositorio de conocimiento para arquitectura de soluciones, ingeniería, proveedores y arquitectura empresarial.

# Estructura propuesta de la Wiki
## SDA - Sistema Documental de Arquitectura

Contenido:

Qué es el SDA.
Alcance.
Objetivos.
Roles.
Cómo navegar la documentación.
Modelo de gobierno.

Basado en la visión general y propósito del SDA.

## 2. Gobierno de Arquitectura
### Roles y Responsabilidades
Arquitecto Empresarial
Arquitecto de Negocio
Arquitecto de Soluciones
Líder Técnico
Gestión de Demanda
Fábricas de Software

Alineado con el modelo de gobierno definido para arquitectura e ingeniería.

## 3. Arquitectura de Negocio
Procesos
Servicios
Actores
Value Streams

## 4. Arquitectura de Aplicaciones
### 4.1 Catálogo de Sistemas

Página por cada sistema:

Ejemplo:

COBIS
Propietario
Descripción
Estado
Tipo despliegue
Integraciones
APIs
Repositorios
Diagramas

La información puede alimentarse desde el catálogo de sistemas definido por el SDA.

## 5. Arquitectura de Datos
### 5.1 Catálogo de Datos

Para cada entidad:

Definición
Dueño del dato
Sensibilidad
Sistema origen
Sistemas consumidores
5.2 Gobierno de Datos
Políticas
Clasificación
Calidad
Linaje

### 5.3 Flujos de Datos

Representación visual derivada de:

matriz_flujos_datos

## 6. Arquitectura Tecnológica
### 6.1 Catálogo Tecnológico
Plataformas
Bases de datos
Middleware
Cloud
Redes

### 6.2 Estándares Tecnológicos

Basado en la SIB:

- Approved, Proposed, Provisional, Phasing-Out, Retired.

## 7. Arquitectura de Integración
### 7.1 Mapa de Integraciones

Generado desde:

matriz_integraciones

### 7.2 Catálogo de API

Por cada API:

- Descripción
- Consumidores
- Productores
- Contrato OpenAPI
- Versiones
- Estado

La iniciativa de API Manager y la estrategia de apificación encajan directamente en esta sección.

## 8. Arquitectura de Soluciones
### 8.1 Soluciones por iniciativa

Cada iniciativa tendría:

- Contexto
- Problema
- Alcance
- Arquitectura objetivo
- Diagramas
- ADR
- Repositorios

### 8.2 Soluciones estratégicas

Ejemplos:

- API Manager
- Azure DevOps ALM - CI/CD
- Modernización ESB
- Sistema Documental Arq.

### 9. Architecture Decision Records (ADR)

Registro de decisiones relevantes de cada transición.

Estructura
ADR-0001

Título

Uso de Azure Repos como repositorio oficial de arquitectura

Estado

Aprobado

Contexto

...

Decisión

...

Consecuencias

...

La estrategia Archi + Azure Repos y ADR ya está contemplada en la documentación de Azure.

## 10. Transiciones Arquitectónicas

Basado en:

- Baseline
- Transition
- Target

Para cada iniciativa:

- Estado actual (as is)
- T1
- T2... 
- Estado objetivo (to be)
- Riesgos
- PUnto de control / Criterios de transición (gates)

## 11. Brechas y Roadmap

Basado en:

matriz_brechas_soluciones_gobierno

Por dominio
- Negocio
- Datos
- Aplicaciones
- Tecnología
- Gobierno

## 13. Conocimiento Operacional

Documentación operativa como:

- Manuales
- Guías 
- Procedimientos

## 14. Proveedores y Compliance
Entregables SDA

- Catálogo de Datos
- Catálogo de Sistemas
- Catálogo de Tecnología
- Catálogo de Requerimientos
- Matrices SDA
- Checklist de conformidad
- Vistas de arquitectura
- Seguridad
- Integración
- Datos
- Gobierno

## Recomendación tecnológica

La implementación elegida es:

Azure DevOps Wiki
│
├── Gobierno
├── Arquitectura Empresarial
├── Aplicaciones
├── Datos
├── Tecnología
├── Integraciones
├── Soluciones
├── ADR
├── Roadmap
├── Patrones
└── Operación

Con:

Archi para modelado.
Azure Repos para versionamiento.
Azure Wiki para conocimiento.
Azure Boards para trazabilidad.
Pull Requests para aprobación documental.

Esta propuesta se alinea con la estrategia de gobierno propuesta para Archi + Azure Repos y la gestión de arquitectura como código (AaC).

