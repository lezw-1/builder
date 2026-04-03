# Principles

## Visualization
- Use **draw.io** for all architecture diagrams — store `.drawio` files in `assets/diagrams/`.

## Layered Architecture
- Enforce **strict layer boundaries**: Presentation → Application → Domain → Infrastructure.  
- Dependencies only point **inward** — never import infrastructure details into domain logic.  
- Avoid **circular dependencies** between layers.  
- Use **interfaces at layer boundaries** to allow substitution and decoupling.