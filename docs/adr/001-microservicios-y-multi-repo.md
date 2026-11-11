# ADR-001: Arquitectura de microservicios con un repositorio por servicio

- **Estado:** Aceptada
- **Fecha:** 2026-11-10

## Contexto
Wiki Wiki Sex Shop es una tienda en línea real que también sirve como proyecto de práctica profesional. Se busca replicar la forma de trabajar de equipos de desarrollo en empresas, con un stack actual: Java, Spring Boot, PostgreSQL, Angular, Docker y Kubernetes.

## Decisión
- Se construirá con microservicios: autenticación, catálogo, pedidos y pagos, detrás de un API Gateway.
- Cada servicio tendrá su propio repositorio y su propia base de datos.
- Los repositorios viven en la organización wikiwiki-shop de GitHub, con la rama main protegida y cambios mediante pull request.

## Alternativas consideradas
- **Monolito modular:** más rápido de construir y operar, pero no permite practicar despliegue independiente, comunicación entre servicios ni orquestación con Kubernetes.
- **Monorepo con microservicios:** más cómodo al trabajar solo, pero se aleja de cómo operan la mayoría de los equipos y de la práctica de pipelines independientes.

## Consecuencias
- Mayor complejidad de infraestructura, configuración y pruebas.
- Hay que cuidar la consistencia de datos entre servicios y los contratos de las APIs.
- Cada servicio se puede desarrollar, probar y desplegar por separado.
- Los repositorios son públicos por ahora (plan gratuito de GitHub): no se suben secretos ni datos reales.
