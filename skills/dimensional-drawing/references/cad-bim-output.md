# CAD/BIM interoperability and output reference

Use this guide when source or delivery formats include CAD, BIM, survey, GIS, or vector drawing files.

## Inspect before converting

Identify the actual file type, software/version where known, units, coordinate system, model origin, levels, layers/categories, linked references, and intended output. Do not claim to have inspected data that was not accessible.

## Geometry and data preservation

- Preserve units and coordinate reference systems; do not reset origins or transform coordinates without an explicit, documented reason.
- Keep source geometry and generated annotations distinguishable.
- Retain useful layer/category names, object IDs, levels, grids, and references when the toolchain supports them.
- Record conversions, simplifications, unsupported entities, and lost metadata.
- For large raster/survey files, use block/windowed access when supported rather than assuming the entire file can be loaded into memory.

## Output capability

- HTML/SVG is appropriate for browser-viewable vector sheets and review diagrams.
- PDF is appropriate for plotted sheets only when a PDF renderer/converter is available and the result has been inspected.
- DXF/DWG, IFC, RVT, and other native formats require a compatible generator/editor or an explicit export workflow. Never rename an SVG/PDF to imply that it is a native CAD/BIM model.
- When native format creation is unavailable, offer a validated vector or tabular intermediate and explain what would be required for a native export.

## QA before delivery

Check sheet extents, units, scale, line types, fonts, clipping, references, coordinate system, and whether the exported file reopens in a compatible viewer. Report what was actually validated and what remains untested.
