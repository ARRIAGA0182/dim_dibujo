---
name: dimensional-drawing
description: Create clear, dimensionally consistent technical drawings for UI components, physical products, architecture, structural engineering, civil infrastructure, and building services. Use for plans, elevations, sections, construction details, reinforcement drawings, profiles, dimensional documentation, or drawing coordination.
---

# Dimensional drawing

Create technical drawings that communicate geometry, dimensions, construction intent, and verification status. The default deliverable is a self-contained HTML file with vector SVG drawing sheets; use another output format only when the available tools can actually create and validate it.

This skill supports five modes:
1. **UI components** — layout anatomy, spacing, radii, layers, and responsive behavior.
2. **Physical products** — orthographic views, sections, parts, and published dimensions.
3. **Architecture** — site plans, floor plans, roof plans, elevations, sections, schedules, and construction details.
4. **Structural engineering** — foundation layouts, concrete and steel elements, reinforcement details, connections, and schedules based on supplied or verified engineering data.
5. **Civil engineering and building services** — grading, roads, longitudinal profiles, cross-sections, water supply, drainage, pipe networks, and related infrastructure.

For a multidisciplinary task, coordinate the relevant modes and keep each drawing's scope and status explicit.

## 1. Source, evidence, and safety rules

1. **Never invent project dimensions, structural reinforcement, material grades, soil data, elevations, pipe sizes, slopes, code requirements, or manufacturer specifications.** Use the supplied model/drawings, verified source data, calculations, or applicable published references. Unknown or unverified items must be marked [TBD] or [VERIFY].
2. **Distinguish facts from assumptions.** Include a short assumptions list when a preliminary schematic must proceed with incomplete information. Never disguise assumptions as measured or approved values.
3. **Resolve conflicts visibly.** If two sources disagree, label the conflict and identify both values/source references; do not silently choose one.
4. **Do not imply engineering approval.** A generated drawing is not a sealed, permitted, or construction-ready design unless the responsible professional has verified and approved it. Do not claim code compliance without the applicable jurisdiction, edition, criteria, and checks.
5. **Do not derive safety-critical details from appearance alone.** In particular, do not guess footing sizes, bar diameters or spacing, concrete strength, welds, connections, cover, anchorage, seismic detailing, pipe pressure class, or earthwork slopes.
6. **Respect source hierarchy:** approved project documents and supplied model data first; verified calculations and authoritative project references next; manufacturer or official standards data when relevant; visual estimation only for illustrative geometry and clearly labelled as such.
7. **State the deliverable's status:** conceptual, preliminary, coordination, review, or issued-for-construction only when that status is supplied and justified by the workflow.

## 2. Choose the drawing mode

Before drawing, identify the requested discipline, intended use, and source:

- Architecture: building type, site/context, required plans/views, levels, units, scale, applicable jurisdiction, and supplied architectural information.
- Structural: design basis, structural system, member geometry, material strengths, loads/calculations where relevant, reinforcement schedules, and responsible engineer's details.
- Civil/infrastructure: survey/topography, coordinate reference system, stationing, elevations, gradients, utility data, pipe/material specifications, and design criteria.
- UI/product: actual source/model, component state, published dimensions, or measurable reference.

If the user has not provided everything, continue with the information available where useful, but list missing inputs and mark affected geometry or notes [TBD]. Ask only for missing information that materially changes the drawing. Do not present a schematic as a complete construction package.

Read the matching reference guide when relevant:
- Architecture: references/architecture.md
- Structural engineering: references/structural-engineering.md
- Civil engineering and infrastructure: references/civil-infrastructure.md
- CAD/BIM interoperability and output: references/cad-bim-output.md

## 3. Universal drawing rules

1. **Scale and units are explicit.** Declare the intended sheet scale and units in the title block. Do not confuse model units, displayed dimensions, screen pixels, and plotted scale. Use a consistent unit system on each sheet; convert only when labelled.
2. **Known construction dimensions are shown as readable values.** Do not force every architectural or engineering dimension to be an abstract code. Use actual supplied/verified values on construction drawings. Use variable codes and formulas for parametric components, repeated systems, or dimensions that need a traceable schedule.
3. **Every dimension must have provenance.** It must be supplied, measured from a reliable model/source, or derived by a transparent calculation. Mark references and derived values when needed.
4. **No false precision.** Round only according to the source accuracy and intended use. Do not add decimal places that imply unsupported survey or manufacturing accuracy.
5. **Views agree.** Plans, elevations, sections, details, schedules, and notes must describe the same geometry and revision.
6. **Readable line hierarchy.** Distinguish cut elements, visible edges, hidden edges, axes/centerlines, dimensions, leaders, hatches, existing work, and proposed work using lineweight and line pattern. Use grayscale/monochrome by default; use color only when requested or required by a documented project convention.
7. **Consistent annotations.** Keep dimension strings outside geometry where possible, avoid crossing labels, align related dimensions, and use consistent arrowheads, text heights, symbols, and leader styles.
8. **Reference every detail.** Detail callouts, section marks, grid labels, level markers, schedules, and sheet references must resolve to real items. Never leave a dangling reference.
9. **Separate design data from presentation.** A visually polished sheet must not hide missing calculations, uncertain dimensions, or unresolved coordination issues.
10. **Keep drawings legible at the intended output size.** Do not shrink text or compress the sheet just to fit everything on one page. Use additional sheets when needed.

## 4. Architecture and engineering workflow

1. **Confirm scope.** Identify discipline, drawing purpose, audience, status, expected views, and output format.
2. **Inspect inputs.** Read supplied sketches, images, PDFs, CAD/BIM data, survey files, schedules, or specifications. Do not assume an unseen model or source has been inspected.
3. **Build a geometry/data inventory.** List known dimensions, levels, axes, coordinates, materials, components, relationships, and missing information.
4. **Choose sheet organization.** Establish sheet size, scale, orientation, title block, legend, dimension style, lineweight hierarchy, and reference numbering.
5. **Draw the primary view first.** Establish the main plan, elevation, section, profile, or component view. Derive secondary views from the same geometry rather than redrawing them independently.
6. **Add dimensions and references.** Prioritize overall dimensions, locating dimensions, levels, grids/stations, critical details, schedules, and notes.
7. **Run geometric checks.** Check dimension-chain closure, alignment, orthogonality where intended, level consistency, slopes, coordinates, clearances, and view-to-view agreement.
8. **Run discipline checks.** Use the appropriate reference guide. Report unresolved structural, code, hydraulic, survey, or coordination checks instead of implying they passed.
9. **Render and inspect.** Open/render the output at the intended size, inspect for clipped geometry, overlapping annotations, unreadable text, missing fonts, and sheet-boundary collisions. Fix issues before delivery.
10. **Deliver with a concise QA note.** Include output files, source basis, assumptions, unresolved [TBD]/[VERIFY] items, and checks performed/not performed.

## 5. Architecture mode

Select relevant deliverables rather than forcing every view onto one sheet:

- Site/context plan with north arrow, boundaries, access, setbacks, contours, and references when source data is available.
- Floor plans with grids, dimensions, spaces, doors/windows, stairs, level markers, and room/area schedules.
- Roof plans with slope direction and drainage references where provided.
- Elevations with levels, openings, materials/finishes only when specified, and aligned datums.
- Sections with floor-to-floor heights, structural depth only when provided, ground relationship, and detail callouts.
- Enlarged construction details for junctions, stairs, openings, wet areas, roofs, and envelope assemblies.
- Schedules for doors, windows, finishes, rooms, and areas when required.

Keep architectural design intent separate from structural assumptions. Verify the applicable building, accessibility, fire/life-safety, and local planning criteria with the project team; do not invent code dimensions or claim compliance without verification.

## 6. Structural engineering mode

Draw only from supplied/verified design data. Possible deliverables include foundation layouts, footing/pedestal/column details, beams, slabs, walls, steel members, connection details, reinforcement sections, bar schedules, and member tags.

- Show member marks, axes, dimensions, levels, section references, material specifications, and reinforcement notes only when known.
- Keep plan, elevation, section, reinforcement callouts, and schedules coordinated.
- Do not infer bar sizes, bar spacing, concrete strength, cover, hooks, laps, anchorage, welds, bolts, or seismic detailing from a generic example.
- If quantities or bar lengths are calculated, show the method and assumptions, account for bends/laps only when specified, and flag items requiring engineer confirmation.
- Distinguish a drafting/coordination check from a structural calculation or code review.

## 7. Civil engineering and building-services mode

Possible deliverables include site grading, roads, profiles, cross-sections, retaining/drainage details, water supply, sanitary/storm drainage, utility plans, and network schematics.

- Preserve the coordinate reference system, datum, units, stationing convention, and source accuracy of survey/GIS data.
- Label existing and proposed terrain distinctly when both are supplied. Do not invent contours, spot elevations, property boundaries, or underground utilities.
- For profiles, coordinate station, ground elevation, design elevation, slope, vertical geometry, structures, and pipe/infrastructure data as applicable.
- For networks, keep node/structure IDs, connectivity, diameters, materials, invert/center elevations, pressure class, and flow/hydraulic results tied to source data.
- Distinguish schematic diagrams from scaled plans and surveyed/as-built records.
- Do not claim hydraulic, geotechnical, road-design, or code compliance from a drawing-only check.

## 8. Sheet composition and title block

For AEC sheets, include fields when relevant:
- Project and location
- Drawing title and discipline
- Drawing/sheet number and revision
- Date and status
- Scale(s) and units
- Source/model reference
- Prepared/checked/approved fields, using [TBD] if unknown
- Legend, north arrow, coordinate/datum note, or grid/level references as relevant

Use a clear title block and a consistent margin. Prefer a coherent set of sheets over one overcrowded sheet. Detail references should include a unique identifier and a destination sheet/view when known.

For UI/product dimensional sheets, retain the compact one-sheet composition, title block, variable tables, plan view, exploded view, detail views, and notes described below.

## 9. Parametric code system

Use variable codes when they improve traceability, especially for UI components, products, and configurable details. Every code used on a drawing must appear in a table.

| Prefix | Meaning | Examples |
|---|---|---|
| S# | spacing | S1 container pad, S3 stack gap |
| H# / Z# / I# | heights / square sizes / icon size | H1 header-min, Z1 lead |
| B / W | border / width | B border, W width range |
| R# | radius | R1 outer radius, R2 inner radius |
| Y / BL / SP / E# | shadow parameters / envelope | E1 top, E2 side |
| D# | parametric dimension | D1 overall length, D2 clear width |
| X/Y or A/B/1/2 | grid axes when used | axes A–C and 1–5 |
| L# or project level tag | levels, when defined by the project | L00, L01, +0.00 |

Do not reuse a code with a different meaning on the same drawing set. In AEC drawings, follow the project's axis, level, member, and detail-tag convention when one exists.

For parametric drawings, show derived values with a formula and result, for example: H1 = 2·S1 + H3 = 64. For construction drawings, show the verified dimension directly and include a calculation note or schedule only where it adds value.

## 10. Existing UI and physical-product mode

Preserve the original UI/product capabilities:

- UI: measure actual source layout using rendered geometry and computed styles where tools permit; document padding, gaps, radii, responsive behavior, hit targets, layers, and viewport placement. Use slots instead of real copy when text content is irrelevant.
- Physical products: use orthographic views and sections; use first-angle or third-angle projection consistently and identify the convention. Use published specifications only, cite sources, and mark unknown dimensions [TBD].
- UI/product variable tables should list code, variable name, value, and source/derivation when helpful.

For UI source inspection, read the actual repository file, Storybook story, design file, URL, or artifact. If Playwright or a browser is unavailable, do not claim that source was rendered or measured in a browser.

## 11. SVG/HTML drawing kit

When delivering HTML/SVG, prefer vector geometry, embedded styles, accessible labels, and a self-contained file. Keep a single consistent coordinate system per sheet. Use unique IDs for markers, patterns, and clip paths when multiple sheets exist.

For the existing UI/product drawing kit, use one begin(svgId) per sheet with unique arrow-marker and hatch-pattern IDs. Helpers may include:

- dimH(x1,x2,y,ext1Y,ext2Y,label,options) for horizontal dimensions
- dimV(y1,y2,x,ext1X,ext2X,label,options) for vertical dimensions
- callout(px,py,ex,ey,label,direction) for leaders
- rad(cornerX,cornerY,r,corner,label,length) for radius callouts
- nb(x,y,n) for boxed note numbers
- detailRef(cx,cy,r,label,lx,ly) for detail references
- table(x,y,title,rows) for variable tables
- notes(rows) for numbered and general notes

For AEC drawings, use discipline-appropriate dimension chains, levels, grid bubbles, section marks, hatches, station labels, and schedules. Do not force the UI/product helper layout onto an architectural or civil plan if it makes the drawing less legible.

Conventions for UI/product sheets: object outline 1.6 px; dimension lines 0.7 px; extension lines 0.55 px; text uses a white knockout where dimensions cross geometry. Slots are dashed, nested surfaces use light gray fills, and keep-out regions may be hatched. Avoid CSS fill rules that override hatch patterns. Inside transformed groups use vector-effect: non-scaling-stroke.

## 12. Output formats and limitations

- **HTML/SVG:** appropriate for self-contained, browser-viewable technical sheets.
- **PDF:** deliver only when an available conversion/rendering tool has actually produced and allowed inspection of the file.
- **DXF/DWG/IFC/RVT:** create or edit only when the available toolchain supports the requested format. Never describe an SVG/HTML drawing as a native CAD/BIM model.
- When a requested format is unsupported, explain the limitation and provide the closest verified alternative, with dimensions and geometry kept editable where possible.

## 13. Before publishing

Check all applicable items:

- Every dimension is sourced, calculated, or marked [TBD]/[VERIFY].
- Units, scale, datum, projection, coordinate reference system, and drawing status are explicit when relevant.
- Dimension chains close within the stated source precision; any mismatch is reported.
- Plans, elevations, sections, profiles, schedules, and callouts agree.
- All detail references and variable codes resolve.
- No labels overlap, geometry is clipped, or text becomes illegible at output size.
- Unknown structural or code-critical information is not presented as approved.
- The rendered output has been inspected; report if rendering/inspection was not possible.
- The delivery note lists files, assumptions, unresolved items, and checks performed.

To animate a finished dimensional sheet, use the separate dimensional-drawing-motion skill.

Finish with a concise note describing what was drawn, the source basis, the checks performed, and any [TBD]/[VERIFY] items.
