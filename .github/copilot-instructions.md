Repository: NoahJenkins — Copilot instructions

Purpose
- Provide straightforward, repo-specific guidance for future Copilot sessions to quickly understand structure, build/test/lint commands (if present), and conventions used in this repository.

Quick checks (build / test / lint)
- No standardized build, test, or lint scripts were detected in repository metadata (no package.json, pyproject.toml, Makefile, or equivalent). If project files with scripts are added later, add commands here and include how to run a single test (e.g., `npm test -- <testName>` or `pytest path/to/test::test_name`).

High-level architecture (big picture)
- This repository currently functions as a static README-driven personal portfolio with supporting static assets. The primary content is README.md plus image assets under assets/. There is no application source code or runtime service in this repo (no server, frontend framework project, or backend code detected).
- Primary responsibilities for Copilot sessions:
  - Keep README.md and assets/ in sync when updating the portfolio content or images.
  - If converting this repo into an app (Next.js, Node, Python, etc.), treat README.md as the top-level documentation and add build/test/lint scripts and CI updates accordingly.
- CI: GitHub Actions workflow(s) live under .github/workflows (e.g., metrics.yml). When editing CI, update workflows there.

Key conventions (project-specific patterns)
- Asset organization:
  - icons are stored under assets/icons/ and company/project logos under assets/logos/. Add new images to these folders rather than hotlinking external assets.
  - README usage: the repository uses specific icon sizes in README.md — 48x48 for "Current Professional Tech Stack" and 40x40 for "Languages and Tools I Have Used". Light/white logos are given a white background, 8px border-radius, and 4px padding in the README styling.
- Keep image sizing and simple inline style consistent with the README patterns when adding or replacing icons/logos.
- Editor settings: repository contains .vscode/settings.json; respect workspace editor rules when making formatting or linting changes.

AI assistant and tooling configurations found
- No CLAUDE.md, .cursorrules, AGENTS.md, .windsurfrules, CONVENTIONS.md, .clinerules or similar assistant-config files were detected. If adding assistant rules or conventions, add a short summary here and reference the file path.

Where to start for Copilot sessions
- Read README.md and inspect assets/ for any requested content changes.
- Inspect .github/workflows/ for CI changes and .vscode/settings.json for editor conventions.

If this repository evolves
- If the repo gains a project (Next.js, Node library, Python package, etc.), update this file to list concrete build/test/lint commands and how to run a single test. Also add brief notes for any nonstandard tooling (e.g., Bicep/PowerShell deployment steps, Azure infra scripts) and where secrets/credentials are expected (never commit secrets).

Contact / follow-ups
- If anything here should be expanded (more CI detail, example test-run commands, or added assistant config files), update this file and commit the change.
