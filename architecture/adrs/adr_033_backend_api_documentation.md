## ADR 033: Backend API Documentation - drf-spectacular

## Context

For our backend API, we need a documentation tool that provides interactive API exploration, automatic schema generation, and OpenAPI compliance. Since we are using Django and Django REST Framework (DRF), the documentation tool must integrate seamlessly and support schema validation.

### Options

1. drf-spectacular
  - **Pros:**
    - Fully supports OpenAPI 3.0.
    - Provides both Swagger UI and ReDoc for interactive documentation.
    - Seamlessly integrates with Django REST Framework.
  - **Cons:**
    - Requires explicit configuration for schema generation.

2. drf-yasg
  - **Pros:**
    - Well-documented and widely used in DRF projects.
    - Provides Swagger and ReDoc documentaiton.
  - **Cons:**
    - Partial support for OpenAPI 3.0.
    - Less actively maintained than drf-spectacular.

3. Manual API Documentation (Postman Collection, Markdown)
  - **Pros:**
    - Full control over the documentation content and format.
    - Can be shared easily via Postman.
  - **Cons:**
    - Requires manual updates, leading to possible inconsistencies.
    - No interactive UI for testing APIs.

## Decision

We have chosen **drf-spectacular** as our API documentation tool for the backend.

## Status

**Accepted** - This decision supports our focus on providing interactive, automatically generated API documentation.

## Consequences

1. Trade-offs:
  - Requires configuring DRF correctly for schema generation.
  - Some advanced customization options require extra effort.

2. Short-Term:
  - Developers have an up-to-date, interactive API documentation tool.
  - Reduces the overhead of maintaining separate API documentation.

3. Long-Term:
  - Future improvements can include authentication documentation (JWT, OAuth).
  - We will revisit this decision post-MVP if better OpenAPI tooling becomes available.
