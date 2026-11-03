# Convenciones de Git

## Ramas
Formato: tipo/WIKI-número-descripcion-corta

Tipos: feature, fix, docs, chore
Ejemplos:
- feature/WIKI-12-login-jwt
- fix/WIKI-20-error-stock
- docs/WIKI-4-convenciones-git

## Commits
Formato: tipo(alcance): descripción [WIKI-número]

Ejemplos:
- feat(auth): agrega login con JWT [WIKI-12]
- fix(catalog): corrige cálculo de stock [WIKI-20]
- docs(git): agrega convenciones de ramas y commits [WIKI-4]

## Reglas
- Nunca se hace push directo a main: todo entra por pull request.
- Cada rama y cada commit referencian su tarjeta de Jira.
- Los pull requests son pequeños y de un solo propósito.
