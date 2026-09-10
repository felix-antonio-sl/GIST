# AGENTS.md

## Misión

Custodiar una copia de trabajo, trazable y privada de la distribución oficial de la ontología `gist` de Semantic Arts para análisis, modelamiento y futuras extensiones con namespace propio.

## Entrada y autoridad

- Usa [`README.md`](README.md) como entrada humana y lee solo las fuentes de `docs/`, `migration/` y `ontologies/` necesarias para la tarea.
- La autoridad semántica de la ontología es el release oficial de Semantic Arts. La copia actual corresponde a `gist 14.1.0`; la procedencia exacta está registrada en el README.
- `ontologies/`, `docs/`, `migration/` y `LICENSE.txt` son materiales extraídos del paquete upstream. No los edites manualmente como si fueran una fuente local independiente.
- `README.md`, `AGENTS.md` y `.gitignore` son entradas operativas propias de este repositorio y no forman parte del release upstream.
- El identificador persistente de carga de `gistCore` es <https://w3id.org/semanticarts/ontology/gistCore>; no lo confundas con una copia local versionada.

## Curaduría y estructura

- Conserva el paquete release completo: serializaciones Turtle, RDF/XML y JSON-LD, módulos complementarios, documentación y migraciones.
- Trata `ontologies/turtle/gistCore14.1.0.ttl` como la representación principal para lectura humana y revisión; las otras serializaciones son entregas upstream que deben mantenerse coherentes con el mismo release.
- Las extensiones de dominio y los términos nuevos deben vivir en un namespace propio. No definas términos locales en el namespace de gist.
- Una actualización debe descargarse en un directorio temporal, comprobarse, registrar versión, fecha, URL y hash, y revisarse contra la copia anterior antes de reemplazarla.
- No hay código ejecutable del producto en este repositorio. Las consultas SPARQL de `migration/` son materiales de migración y no deben ejecutarse sobre datos reales sin una revisión explícita del contexto y del destino.
- No añadas PII, PHI, secretos, credenciales ni datos de producción al corpus.

## Verificación

Desde la raíz del repositorio:

```sh
git status --short
git diff --check -- README.md AGENTS.md .gitignore
find ontologies -type f -print | sort
rg -n '14\.1\.0|w3id\.org/semanticarts/ns/ontology/gist/' ontologies docs/markdown/README.md
```

La distribución upstream conserva finales de línea CRLF en sus archivos de
release; por eso el `diff --check` focalizado se limita a las entradas
operativas locales y no reescribe el contenido descargado.

Comprueba por separado la validez formal de cada serialización con el parser o reasoner que vaya a consumirla. La presencia de los archivos, sus nombres o un hash no demuestra por sí sola la corrección semántica ni el comportamiento de una herramienta externa.

## Seguridad y entrega

- Mantén este repositorio privado salvo autorización explícita para cambiar su visibilidad.
- No publiques, instales ni modifiques consumidores de gist fuera de este repositorio como parte de una actualización local.
- Antes de declarar una actualización lista, revisa el diff completo, la licencia, la procedencia y la coherencia de versión entre las tres serializaciones.
