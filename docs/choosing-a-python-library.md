# Choosing a Python Library

How to evaluate a Python package before depending on it — and per-category picks from the [catalog](../README.md).

## Maintenance signals (check before you adopt)

1. **Release cadence.** A healthy library ships regularly. Check the GitHub releases page or PyPI history: no release in 2+ years is a yellow flag (exceptions: finished, stable tools like `httpx` in maintenance mode — stable is fine, abandoned is not).
2. **Commit activity.** Recent commits on the default branch mean someone is home. Archived repos are dead — don't build on them.
3. **Issue/PR responsiveness.** A mountain of unanswered issues with no maintainer replies is a red flag, even with recent releases.
4. **Bus factor and governance.** Single-maintainer projects can be excellent (they often are) but carry continuity risk; foundation-backed projects (PSF, PyPA, NumFOCUS) have institutional backing.
5. **Python version support.** Check `requires-python`: a library stuck below 3.10 in 2026 is probably unmaintained. Also check for free-threading (3.13t) and GraalPy/PyPy support if you care.
6. **Typing.** `py.typed` marker + passing mypy/pyright strict is a quality signal; untyped libraries are harder to use safely at scale.
7. **Security posture.** For anything network-facing: check for a published security policy and CVE history.

## Per-category picks (opinionated starting points)

- **Web API:** FastAPI for typed, OpenAPI-first APIs; Django when you need the full stack (ORM, auth, admin); Flask for minimal services.
- **HTTP client:** httpx (sync + async, HTTP/2); requests remains fine for simple sync scripts.
- **Async:** asyncio is the stdlib default; trio for structured concurrency; anyio to write backend-agnostic code.
- **ORM:** SQLAlchemy for full power and flexibility; Django ORM inside Django; Tortoise/Piccolo for async-first greenfield.
- **Background jobs:** Celery for the full-featured distributed case (actively maintained); RQ for simple Redis-backed queues; APScheduler for in-process scheduling.
- **DataFrames:** Polars for new work (fast, Arrow-native); pandas where the ecosystem (the long tail of `pd.`-based code) demands it.
- **ML:** scikit-learn for classical ML; PyTorch for deep learning research and most production DL; JAX for composable transforms and TPU work; XGBoost/LightGBM for tabular data.
- **Notebooks:** JupyterLab as the primary environment; Marimo if you want notebooks-as-scripts with reactivity.
- **Testing:** pytest, full stop. Add Hypothesis for property-based tests, coverage.py for coverage, tox/nox for matrix testing.
- **Packaging:** uv is the fast modern default; Poetry and Hatch remain solid; pip + virtualenv is the timeless baseline.
- **Lint/format/type:** Ruff (linter + formatter, very fast); mypy or pyright for static typing; pydantic for runtime validation.
- **CLI:** Typer for typed CLIs, Click for full control, Rich/Textual for terminal UIs.
- **Scraping:** Scrapy for crawling at scale; Playwright/Selenium for real-browser automation; Beautiful Soup for quick parsing.

## Performance notes

- Pure-Python speed rarely matters; what matters is whether the hot path drops into C/Rust (NumPy, Polars, pydantic-core, Ruff, uv all do).
- For CPU-bound parallelism, the GIL is the wall: multiprocessing, C extensions that release the GIL, or free-threaded Python 3.13+ are the exits.
- Async helps I/O-bound workloads only — it does nothing for CPU-bound code.
