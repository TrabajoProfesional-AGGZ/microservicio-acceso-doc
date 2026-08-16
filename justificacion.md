---
layout: default
title: Justificación tecnológica
nav_order: 3
---

# 🛠️ Justificación tecnológica

En esta sección documentamos las decisiones técnicas tomadas para la construcción del microservicio de accesos, asegurando que cada herramienta elegida aporte valor real al desarrollo y mantenimiento del producto.

## Lenguajes y frameworks

Para este microservicio, la selección de nuestra pila tecnológica se basó en la agilidad, la escalabilidad y la facilidad de mantenimiento continuo:

* **Python:** Se eligió como lenguaje principal por su sintaxis clara, curva de aprendizaje rápida y su excelente manejo de operaciones de red y estructuración de datos.
* **FastAPI:** Seleccionado como framework web por su rendimiento de clase mundial (soporte asíncrono nativo). Su mayor ventaja para este proyecto es la validación estricta de datos y la autogeneración de documentación interactiva (Swagger/OpenAPI), lo cual garantiza que los contratos de la API estén siempre sincronizados con el código.
* **SQLAlchemy y Alembic:** Implementados como ORM y herramienta de migraciones respectivamente. Permiten un modelado robusto de la base de datos (tablas de accesos y secretos) y un control de versiones de esquema seguro e incremental.
* **Pytest:** Adoptado como nuestro framework de pruebas. Su ecosistema, simplicidad y uso de *fixtures* nos permite escribir tests escalables y legibles.
* **Docker y Docker Compose:** La contenerización es indispensable en nuestra arquitectura. Nos permite aislar el microservicio y garantizar la paridad exacta entre entornos (desarrollo, *staging* y producción).

## Integración y despliegue continuo (CI/CD)

La implementación de pipelines de CI/CD (vía GitHub Actions) es fundamental en el microservicio para garantizar entregas ágiles y seguras. Nos permite automatizar la ejecución de pruebas y el despliegue a los distintos entornos, reduciendo el error humano y acelerando el *time-to-market*.

## Pruebas unitarias y Code Coverage

Para asegurar la robustez y estabilidad del código, mantenemos un estándar estricto de calidad:

* Se ha implementado una gran cantidad de pruebas unitarias cubriendo los casos de uso principales y casos borde.
* Utilizamos **Codecov** integrado en nuestro pipeline para mantener un estricto nivel de Code Coverage (cobertura de código), validando automáticamente los estándares de calidad en cada Pull Request antes de su integración a la rama principal.

## Documentación integral

Utilizamos **JustTheDocs** para mantener esta documentación viva, versionada junto con el código y fácilmente accesible para cualquier miembro del equipo. Esto centraliza el conocimiento y reduce los cuellos de botella en la comunicación.
