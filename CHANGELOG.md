# Changelog

## 1.1.1 (2026-11-16)

- **Fix: pytest collected the code cloned into `resources/code/`**, so `uv run python -m pytest` failed on a cloned repository's own tests and dependencies. `testpaths = ["tests"]` in `pyproject.toml`.

## 1.1.0 (2026-11-16)

- **Fix: Zotero lookups by citekey.** Zotero's search never matches a citekey, so `fetch` never got a PDF from Zotero, attaching a PDF failed with "no item with the citekey", and a new citekey could collide with one already in the library. The library's top-level items are now listed once and the citekey read from them. Backported from the [research knowledge tree](https://github.com/bonneted/research-knowledge-tree) (9817c43).
- README: links to the public knowledge tree; "When to move to the knowledge tree".
- `LICENSE` and the fetch User-Agent use the template's name.

## 1.0.0 (2026-11-12)

First release: the light v1 of the research knowledge tree. Sources → wiki ← code, the `digest-source` and `update-wiki` skills, the `fetch` and `refs` commands, `docs/notes/` and `resources/inbox/`.
