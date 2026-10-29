<p align="center">
  <img src="assets/dialog-motion.gif" alt="A dimensional drawing sheet being drawn and animated" width="100%">
</p>

<h1 align="center">dim_dibujo ✏️📐</h1>

<p align="center">
  <b>Dimensional drawing for interfaces, architecture, and engineering.</b><br>
  Create clear, traceable technical sheets with coordinated views, dimensions, details, and explicit verification status.
</p>

<p align="center">
  <a href="#capabilities">Capabilities</a> ·
  <a href="#install">Install</a> ·
  <a href="#use-it">Use it</a> ·
  <a href="#make-it-move">Make it move</a> ·
  <a href="#examples">Examples</a>
</p>

---

The project began with the visual discipline of dimensional drawings: a clear sheet, multiple views, precise annotations, detail references, and dimensions that can be checked. It now extends that approach to architecture and engineering while preserving the original UI-component and physical-product workflows.

## Capabilities

| Mode | Examples |
|---|---|
| **UI components** | Layout anatomy, spacing, radii, layers, responsive behavior, and viewport placement |
| **Physical products** | Orthographic views, sections, part details, and published dimensions |
| **Architecture** | Site plans, floor plans, roof plans, elevations, sections, schedules, and construction details |
| **Structural engineering** | Foundation layouts, concrete and steel members, reinforcement details, connections, and schedules based on verified design data |
| **Civil engineering and services** | Grading, roads, profiles, cross-sections, water supply, drainage, utility plans, and infrastructure details |

The skill uses discipline-specific reference guides so an agent can load the guidance relevant to the requested drawing.

## What's inside

~~~
skills/
├── dimensional-drawing/
│   ├── SKILL.md
│   ├── examples/                 Existing UI component sheets (HTML)
│   └── references/
│       ├── architecture.md
│       ├── structural-engineering.md
│       ├── civil-infrastructure.md
│       └── cad-bim-output.md
└── dimensional-drawing-motion/   Animates a finished sheet
    ├── SKILL.md
    ├── templates/
    └── adapters/
~~~

## Drawing principles

- **Traceable dimensions:** use verified values or transparent derivations; mark unknowns [TBD] or [VERIFY].
- **Coordinated views:** plans, elevations, sections, details, profiles, and schedules must agree.
- **Explicit scale and units:** do not confuse model units, pixels, and plotted dimensions.
- **Readable technical hierarchy:** lineweights, hatches, dimensions, labels, and references remain legible at output size.
- **No invented engineering data:** structural, geotechnical, hydraulic, survey, or code-critical values must come from the project source or a verified method.
- **Honest deliverable status:** a drawing-only consistency check is not structural analysis, code approval, or professional sign-off.

For parametric UI/product drawings, variable codes and formulas are used when they improve traceability. For architectural and engineering drawings, verified construction dimensions are shown directly where appropriate.

## Install

Clone this repository and copy the skills you need.

**Claude Code**

~~~bash
git clone https://github.com/ARRIAGA0182/dim_dibujo.git
cp -r dim_dibujo/skills/* ~/.claude/skills/
~~~

**claude.ai / Claude desktop:** zip the required skill folder (for example, skills/dimensional-drawing) and add it under Settings → Capabilities → Skills, where supported by your account.

**Other agents:** point the agent to the relevant SKILL.md and its reference files, or use a compatible skills installer.

## Use it

Provide a source and describe the required drawing, intended use, units, scale, and output format. Useful examples:

- “Create a dimensioned architectural floor plan from these supplied measurements. List any missing dimensions.”
- “Create a section and reinforcement-detail sheet from this approved structural detail. Do not infer missing bar sizes or spacing.”
- “Create a longitudinal profile for this water-supply line from the supplied stations and elevations. Preserve the coordinate and vertical datum.”
- “Create a dimensional drawing of the Card component in the source repository.”
- “Draw the anatomy of this dialog component using the existing monochrome style.”

The skill can create self-contained HTML/SVG sheets when suitable tools are available. Native DWG, DXF, IFC, or RVT output depends on the available compatible toolchain; the skill must not claim to have created or validated a native file when it has not.

## Make it move

The separate dimensional-drawing-motion skill animates a finished sheet like a pen drawing it while the camera moves across the paper.

- With a compatible Motion artifact workflow, export the finished animation as MP4.
- For the headless renderer, see skills/dimensional-drawing-motion/adapters/headless; it requires the documented runtime dependencies.

Animation is a presentation layer. It does not replace dimension checks or discipline review.

## Examples

The current HTML examples demonstrate the original UI-component workflow:

- [Dialog sheet](skills/dimensional-drawing/examples/dialog-sheet.html)
- [Card sheet](skills/dimensional-drawing/examples/card-sheet.html)

The architecture and engineering reference guides define conventions and QA rules; they do not claim that discipline-specific sample drawings or native CAD/BIM exporters are included.

## Credits and license

The original UI/product drawing approach was inspired by [Apple's accessory dimensional drawings](https://developer.apple.com/accessories/dimensional-drawings/) and [Andreas Storm](https://x.com/avstorm).

See the repository LICENSE for licensing terms.
