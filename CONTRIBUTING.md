# Contributing

Thanks for helping curate this markdown-first repository.

## Pull request basics

* Keep changes focused and small.
* Add or update links with a short, useful description.
* Place new entries in the expected section and keep ordering consistent.
* Remove dead or duplicated links when you find them.

## Quality checks

* Markdown files should avoid trailing whitespace and repeated blank lines.
* Added or updated links should be reachable.
* JSON files in `data/` should parse with `python3 -m json.tool`.
* CI validates markdown hygiene and links on pull requests.

## Agent-facing context

When changing newcomer guidance or canonical resources, keep these files in sync:

* `README.md`
* `AGENTS.md`
* `llms.txt`
* `data/starter-paths.json`
* `data/resource-index.json`
