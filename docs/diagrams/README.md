# Diagrams

Interactive diagrams generated with [Archify](https://github.com/tt-a1i/archify).
Open the `.html` files in any browser: no install needed. They support pan/zoom, search, guided views, light/dark themes and PNG/SVG export.

| Diagram | HTML | Source spec |
|---|---|---|
| System architecture | [system-architecture.html](system-architecture.html) | [system-architecture.architecture.json](system-architecture.architecture.json) |
| System flow (indexing + Q&A loop) | [system-flow.html](system-flow.html) | [system-flow.workflow.json](system-flow.workflow.json) |
| Data flow loop (animated) | [data-flow-loop.html](data-flow-loop.html) | [data-flow-loop.dataflow.json](data-flow-loop.dataflow.json) |

## Regenerating

Edit the JSON spec, then run from a checkout of the Archify skill folder:

```bash
node bin/archify.mjs deliver architecture <repo>/docs/diagrams/system-architecture.architecture.json \
  <repo>/docs/diagrams/system-architecture.html --quality showcase --repo-root <repo>
node bin/archify.mjs deliver workflow <repo>/docs/diagrams/system-flow.workflow.json \
  <repo>/docs/diagrams/system-flow.html --quality showcase
node bin/archify.mjs deliver dataflow <repo>/docs/diagrams/data-flow-loop.dataflow.json \
  <repo>/docs/diagrams/data-flow-loop.html --quality showcase
```
