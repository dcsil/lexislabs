## ADR 017: Backend Technology and Framework - Python Django

## Context

For our MVP, we need a backend framework that supports rapid development, easy integration with AI tools, and scalability. Since Python is a natural choice for AI/ML workflows, the backend framework must complement this ecosystem and simplify our MVP development.

### Options

1. **Python Django**  
   - **Pros**:  
     - Comes with built-in tools like ORM, authentication, and admin dashboards, reducing setup time.  
     - Strong compatibility with Python AI libraries like Cohere and OpenAI.  
   - **Cons**:  
     - Slightly heavier compared to lightweight frameworks like FastAPI.  

2. **Node.js (with Express)**  
   - **Pros**:  
     - Lightweight and fast for handling APIs and asynchronous tasks.  
     - Consistent with our frontend since both use JavaScript/TypeScript.  
   - **Cons**:  
     - Lacks built-in tools, requiring more effort to set up essentials like authentication.  

3. **FastAPI (Python)**  
   - **Pros**:  
     - Optimized for building APIs and supports asynchronous operations.  
     - Lightweight and integrates well with Python AI tools.  
   - **Cons**:  
     - Missing many built-in features Django offers, which would require additional development effort.

## Decision

We have chosen **Python Django** as the backend framework for NeuroLingo.

## Status

**Accepted** - This decision supports our focus on rapid MVP development and seamless AI integration.

## Consequences

1. **Trade-offs**:
   - Django’s heavier framework might introduce some inefficiencies for smaller components.

2. **Short-Term**:
   - Faster development due to Django’s built-in tools.  
   - Easy integration with Python-based AI libraries.

3. **Long-Term**:
   - We’ll revisit this decision post-MVP if we face scalability challenges or need to focus on specific API features.  
