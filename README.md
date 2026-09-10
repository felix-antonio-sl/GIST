# GIST

Repositorio privado de trabajo para la ontología superior empresarial `gist` de Semantic Arts. Esta copia contiene el paquete oficial `gist 14.1.0`, descargado el 10 de septiembre de 2026, con sus serializaciones, documentación y materiales de migración.

## Orientación

- Ontología principal en Turtle: [`ontologies/turtle/gistCore14.1.0.ttl`](ontologies/turtle/gistCore14.1.0.ttl).
- Serializaciones equivalentes: [`ontologies/rdf-xml/`](ontologies/rdf-xml/) y [`ontologies/json-ld/`](ontologies/json-ld/).
- Módulos complementarios: `gistMediaTypes`, `gistPrefixDeclarations`, `gistRdfsAnnotations` y `gistSubClassAssertions`.
- Documentación y notas de versión: [`docs/markdown/`](docs/markdown/).
- Guías y consultas para migraciones mayores: [`migration/`](migration/).

La página oficial de Semantic Arts es el punto de entrada conceptual: <https://www.semanticarts.com/gist/>. Para cargar el identificador persistente de `gistCore` en una herramienta de ontologías se puede usar <https://w3id.org/semanticarts/ontology/gistCore>.

## Procedencia de esta copia

| Dato | Valor |
| --- | --- |
| Release | `gist 14.1.0` |
| Tag upstream | [`v14.1.0`](https://github.com/semanticarts/gist/releases/tag/v14.1.0) |
| Commit del tag upstream | `c73068bfe779db2643b1e43c920cc8039b15a013` |
| Paquete descargado | <https://downloads.semanticarts.com/gistCore_Current_Version.zip> |
| `Last-Modified` observado | `2026-04-23T21:56:59Z` |
| SHA-256 del ZIP descargado | `9be97c9a99b9ccd7cdd986a02a8f4eb794bc3ffa83204b7c1437cad63f5d7ded` |
| Fecha de descarga | `2026-09-10` |

El paquete fue extraído conservando su estructura. Los archivos bajo `docs/`, `migration/`, `ontologies/` y `LICENSE.txt` son materiales de la distribución upstream; el `README.md` y el `AGENTS.md` de esta raíz son documentación operativa local de esta copia.

## Licencia y uso

El material upstream se distribuye bajo [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/); la copia de la licencia está en [`LICENSE.txt`](LICENSE.txt). Mantén la atribución a Semantic Arts y respeta las condiciones indicadas por la fuente: los términos de gist permanecen en su namespace y las extensiones deben usar un namespace propio.

Este repositorio privado contiene la distribución descargada; no es el repositorio upstream ni implica que una modificación local haya sido aceptada por Semantic Arts. Para actualizar la ontología, descarga un nuevo release, conserva su procedencia y revisa el diff de todas las serializaciones antes de sustituir la copia vigente.
