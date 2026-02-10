# GitHub Profile Repository Guidelines

This is a GitHub profile README repository showcasing Noah's professional experience, skills, and certifications.

## Repository Purpose

- **Primary file**: [README.md](../README.md) - the GitHub profile page displayed at github.com/NoahJenkins
- **Auto-generated assets**: `github-languages.svg` (language statistics chart)
- **Automated workflow**: [.github/workflows/metrics.yml](.github/workflows/metrics.yml) generates metrics daily at 06:00 UTC

## Markdown Conventions

- **HTML allowed**: `.markdownlint.json` disables MD033 to permit inline HTML styling for logos and badges
- **Logo formatting**: Company logos use `height="45"` with white background, `border-radius: 8px`, and `padding: 4px`
- **Tech icons**: Current stack uses `width="48" height="48"`, general tools use `width="40" height="40"`
- **Badge style**: Certification badges use shields.io format with appropriate logo and color schemes

## Structure Patterns

### Section Order (README.md)
1. Introduction (bullet points with role, specialties, interests)
2. Where I've Worked (company logos)
3. Tools and Tech (Current Professional Tech Stack → Languages and Tools I Have Used → My Most Used Languages)
4. Certifications (Cloud & DevOps → Security & Identity → Fundamentals & Other)
5. Let's Connect (social links)

### Logo References
- Use CDN sources: `cdn.jsdelivr.net/gh/devicons/devicon`, `upload.wikimedia.org`, or official sources
- Light-themed logos (Next.js, Vercel, Expo) require `style="background-color: white; border-radius: 8px; padding: 4px;"`

## GitHub Actions Workflow

The `metrics.yml` workflow:
- Runs on push to main/master, manual dispatch, or daily schedule
- Uses `lowlighter/metrics@latest` action to generate `github-languages.svg`
- Auto-commits generated files back to the repository
- Requires `METRICS_TOKEN` secret (GitHub personal access token)

### When Removing Features
- Update both README.md display sections AND workflow generation steps
- Adjust `file_pattern` in commit step to match generated files

## Editing Guidelines

- **Profile updates**: Modify README.md directly - content is self-documenting
- **New certifications**: Add to appropriate category using existing badge format pattern
- **Tech stack changes**: Update relevant icon section maintaining established sizing
- **Workflow changes**: Test locally or use `workflow_dispatch` before committing schedule changes

## VS Code Configuration

Custom spell-check dictionary includes GitHub Action author names and technical terms. Add new proper nouns to `.vscode/settings.json` → `cSpell.words`.
