# Agent Guide

This repository is a curated BSD map, not a link dump. Agents should optimize for current, useful, canonical resources and make the list easier for humans and other agents to navigate.

## Goals

* Make `README.md` useful for a newcomer who knows little about BSD.
* Prefer official documentation, project pages, foundations, manpages, and active communities.
* Preserve historically useful resources only when they are clearly labeled or placed away from newcomer paths.
* Keep machine-readable context in sync with prose.

## Editing Rules

* Check each added or changed URL with redirects enabled.
* Do not add links that require fragile scraping, login, or JavaScript-only rendering unless there is no better canonical source.
* If a resource is inactive, niche, historical, or research-focused, say so directly.
* Do not add dependency-heavy tooling. Repo automation should use standard shell/Python or MIT/BSD/Apache-2.0 licensed actions/tools.
* Keep descriptions short, factual, and non-marketing.
* For newcomer-facing entries, explain who should use the resource.

## Required Checks

Run these before committing:

```sh
git diff --check
python3 -m json.tool data/starter-paths.json >/dev/null
python3 -m json.tool data/resource-index.json >/dev/null
```

Also run the markdown whitespace check from `.github/workflows/docs-quality.yml` or an equivalent local script.

## Curation Priorities

1. Start-here paths and canonical docs.
2. Active general-purpose BSD projects.
3. Practical administration resources: manpages, handbooks, ports/packages, jails, virtualization, filesystems.
4. Active communities and news sources.
5. Niche, research, embedded, or historical resources.

## Common Agent Tasks

* Adding a link: update `README.md`, then add or adjust the relevant entry in `data/resource-index.json` if it is a canonical or high-value resource.
* Changing newcomer guidance: update `README.md`, `llms.txt`, and `data/starter-paths.json`.
* Moving a stale project: preserve the URL only if it still resolves and the historical value is clear.
* Debugging CI: first check `lychee.toml`, then verify whether the target site blocks automation or the URL is actually stale.
