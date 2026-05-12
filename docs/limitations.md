# Known Limitations

[← Back to README](../README.md)

- **Native UML notation**: tldraw arrowheads are limited (no hollow triangles for inheritance). Use drawio-skill for strict UML/ERD figures intended for academic papers
- **No native containers/swimlanes**: tldraw's grouping model differs from drawio. Use color and spacing for visual grouping instead
- **PDF export not supported**: tldraw-cli supports PNG and SVG only. Convert SVG to PDF post-hoc if needed (e.g. `rsvg-convert`)
- **Self-check requires vision**: The auto-fix step reads exported PNGs using the model's vision capability. Models without vision support skip this step
