# Process Improvement Plan Generator

A modern, interactive Lean Six Sigma-based webpage application for building department-specific process improvement plans.

## What it does

- Presents a standard six-step process improvement plan template.
- Generates tailored plans for departments, functions, workflows, or custom topics.
- Includes DMAIC, PDCA, root-cause analysis, KPI monitoring, stakeholder planning, risks, timeline, and control-plan content.
- Provides diagram, detailed plan, and presentation modes.
- Supports browser-based export actions:
  - Download PDF
  - Print View
  - Copy Plan
  - Download Diagram
  - Save as Presentation PDF

## How to use

Open `index.html` in a browser or host the repository as a static site.

Enter a department or process in the generator field, or use one of the quick-select chips. The app will generate a tailored process improvement plan and enable export options for meeting-ready use.

## GitHub Pages deployment

This repository includes a GitHub Pages workflow at `.github/workflows/pages.yml`.

To serve the app at `https://jlijano.github.io/pip/`:

1. Open the repository settings in GitHub.
2. Go to **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Run the **Deploy static site to GitHub Pages** workflow, or push a new commit to `main`.

The site entry point is `index.html` in the repository root. The `.nojekyll` file is included so GitHub Pages serves static assets without Jekyll processing.

## Included departments

- Human Resources
- Sales
- Customer Service
- Operations
- Finance
- IT Help Desk
- Training & Development
- Compliance
- Manufacturing
- Healthcare
- Logistics
- Procurement

Additional custom topics use a Lean Six Sigma fallback model.

## Notes

The PDF and image export features use browser-side libraries loaded from CDN:

- `html2canvas`
- `jsPDF`

If the app is used in an offline or restricted network environment, Print View and Copy Plan remain available, but PDF/image export may require local bundling of those libraries.
