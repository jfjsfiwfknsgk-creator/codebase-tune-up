# AGENTS.md

## Core Service Rules

This repository-improvement service is limited to authorized repository work only.

Codex must:

- Stay within repository scope.
- Use only files, functions, configs, dependency manifests, tests, CI files, documentation, issues, and pull requests that are explicitly authorized.
- Prefer evidence-based findings with concrete file paths and function/class/config names.
- Avoid unsupported severity claims.
- Avoid exploitation, credential use, live-system testing, bypassing protections, stealth automation, aggressive scraping, or external scanning.
- Never claim unauthorized access or live-system validation.
- Produce minimal diffs.
- Preserve project style.
- Avoid touching unrelated files.
- Run tests when available, or explain why tests could not be run.
- Explain verification steps clearly.
- Prefer low-risk practical improvements that maintainers can review quickly.

## Review Output Rules

Findings must include:

- Evidence
- Impact
- Fix
- Estimated effort
- PR suitability

Limit review output to the top 5 issues unless explicitly asked otherwise.

## Pull Request Rules

A PR should:

- Address one issue only.
- Make the smallest useful change.
- Include tests or documentation updates when practical.
- Include verification steps.
- Include rollback notes.

## Prohibited Work

Do not perform:

- Unauthorized security testing
- Penetration testing
- Exploitation
- Credential use
- Live external system validation
- Third-party infrastructure testing
- Bot evasion
- Stealth browsing
- Automated vulnerability scanning outside repository evidence

## Error Handling

Do not fight repeated errors. If the same error occurs twice, pause implementation, research 3-5 plausible fixes, choose the most efficient safe solution, and continue.
