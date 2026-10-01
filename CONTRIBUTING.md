# Contributing to Awesome-python

Thanks for helping keep this list accurate. This repo has strict honesty rules — please read them before opening a PR.

## What belongs here

- **The general-purpose Python ecosystem**: web frameworks (Django, FastAPI…), async & networking (httpx, trio…), databases & ORMs (SQLAlchemy, asyncpg…), task queues (Celery, RQ…), data science (NumPy, Polars…), machine learning (PyTorch, scikit-learn…), notebooks & visualization, testing, packaging, linting/formatting/typing, CLI & TUI tools, web scraping & automation, and dev tools.
- **LLM-specific Python tooling is out of scope** (LangChain, LlamaIndex, vLLM…) — that lives with the [Awesome-llms-labs](https://github.com/Awesome-llms-labs) family. Core ML libraries (PyTorch, transformers…) stay, since they are foundational Python.

## Entry requirements (all must hold)

1. **Real and verifiable.** The project must exist at the linked URL. `verified` is `true` only if you confirmed the entry on an official source (the project's repo, LICENSE file, or official site) — never from a blog roundup alone.
2. **Honest license.** Copy the SPDX identifier from the project's actual LICENSE file — not from memory, not from the GitHub API's `spdx_id` alone (it reports NOASSERTION for several projects here, e.g. gunicorn, PyTorch). Proprietary products are `"proprietary"` — never imply a paid product is open source. If the license can't be confirmed, set `"license": null`, `"verified": false`, and explain in `"unverified_reason"`.
3. **No invented facts.** No guessed star counts, release dates, or descriptions. If you can't verify it, leave it `null` and say why.
4. **One category each.** Pick the single best-fitting `category`.

## How to add an entry

1. Add the entry to `data/python.json` (keep the file's existing ordering: grouped by category, alphabetical within):
   ```json
   {
     "name": "Example Lib",
     "description": "One-line description, no hype.",
     "license": "MIT",
     "category": "testing",
     "repo": "https://github.com/org/example-lib",
     "homepage": "https://example-lib.readthedocs.io",
     "official_site": "https://example-lib.readthedocs.io",
     "stars": 1234,
     "verified": true,
     "unverified_reason": null
   }
   ```
   Use `null` (not `""`) for unknown `repo`/`official_site`/`stars`/`unverified_reason`.
2. Add the matching bullet to the right section in `README.md`: `- [Example Lib](https://example-lib.readthedocs.io) — one-line description. *(MIT · ⭐ 1,234)*`
3. Run the CI validation locally if you can (`python` 3.12+, see `.github/workflows/ci.yml`): it checks JSON validity, duplicate names/URLs, the README↔JSON cross-check, section counts, and TOC anchors.
4. Open a PR describing what you verified and where (link the official source).

## Link hygiene

- Prefer `https://` URLs; no URL shorteners.
- If a project renamed/moved, update to the canonical URL and note it in `docs/status-changes.md`.

## What gets rejected

- Entries with invented licenses, stars, or descriptions.
- Dead links, or projects you can't confirm exist.
- LLM-specific frameworks (wrong family — they belong to Awesome-llms-labs).
