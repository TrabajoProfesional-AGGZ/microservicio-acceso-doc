---
layout: default
title: Inicio
nav_order: 1
description: "Documentacion del microservicio de accesos de SocioUnido"
---

# Microservicio de accesos

Microservicio encargado de la gestión, validación y auditoría de los accesos físicos y lógicos de "SocioUnido".

## Utilidad y funcionalidad

El microservicio de accesos está diseñado para manejar las siguientes responsabilidades clave:

* **Validación de ingreso:** Verifica en tiempo real las credenciales, carnets o tokens de los usuarios para autorizar o denegar el acceso a las instalaciones físicas o áreas lógicas restringidas de la institución.
* **Registro y auditoría:** Mantiene un historial detallado de las entradas y salidas, permitiendo trazar la actividad de cada socio o empleado dentro de la infraestructura.
* **Gestión de secretos e integraciones:** Administra de forma segura las credenciales (secretos) necesarias para la comunicación con hardware de terceros (ej. molinetes, lectoras QR) y otros sistemas del ecosistema.

## ¿Qué vas a encontrar en esta página?

A continuación, se detalla toda la información técnica, arquitectónica y organizativa sobre esta implementación en particular:

* 🔌 **[Endpoints](endpoints.html):** Documentación estática y detallada de la API, ideal para consultar integraciones.
* 🛠️ **[Justificación tecnológica](justificacion.html):** El porqué de los lenguajes y frameworks elegidos, nuestro pipeline de CI/CD, la estrategia de testing y métricas de Code Coverage definidas.
* 🏗️ **[Arquitectura y diagramas](diagramas.html):** Representación visual de la arquitectura del microservicio utilizando el modelo C4.
* 📊 **[Métricas de la implementación](metricas.html):** Estadísticas del desarrollo, cantidad de commits, Pull Requests y distribución del trabajo en el equipo.
