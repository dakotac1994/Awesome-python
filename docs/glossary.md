# Glossary

Terms you'll meet across the [Awesome-python](../README.md) catalog.

- **GIL (Global Interpreter Lock)** — CPython's mutex that allows only one thread to execute Python bytecode at a time; the reason CPU-bound threads don't scale. Being addressed by free-threaded builds (3.13+) and by releasing the GIL in C extensions.
- **Wheel** — the binary package format pip installs (`.whl`); prebuilt wheels avoid compiling C extensions locally.
- **Virtual environment** — an isolated Python installation (via `venv`, `virtualenv`, or `uv venv`) so project dependencies don't collide.
- **Type hints** — optional annotations (`def f(x: int) -> str`) checked by mypy/pyright and used at runtime by FastAPI, Typer, and pydantic.
- **py.typed** — the marker file that tells type checkers a package ships inline type annotations.
- **WSGI / ASGI** — the sync (WSGI) and async (ASGI) server↔application interfaces; gunicorn serves WSGI, uvicorn serves ASGI.
- **ORM (Object-Relational Mapper)** — maps database rows to Python objects (SQLAlchemy, Django ORM, Tortoise ORM).
- **Migration** — a versioned schema change script (Alembic generates them from model diffs).
- **DataFrame** — the labeled 2-D table structure at the heart of pandas and Polars.
- **Arrow (Apache Arrow)** — the in-memory columnar format enabling zero-copy exchange between pandas, Polars, DuckDB, and others.
- **JIT (just-in-time compilation)** — compiling hot code at runtime (Numba for numerics, PyPy's tracer, mypyc ahead-of-time).
- **Property-based testing** — describing invariants and letting the framework generate cases (Hypothesis), instead of hand-writing examples.
- **Task queue** — background job system: producers enqueue work, workers execute it (Celery, RQ, Dramatiq).
- **Structured concurrency** — the trio/anyio model where child tasks can't outlive their parent scope, making cancellation and error propagation predictable.
- **Lockfile** — a pinned, hash-verified dependency snapshot (`uv.lock`, `poetry.lock`, `pdm.lock`) for reproducible installs.
- **PEP 517/518** — the standards that let any build backend (hatchling, setuptools, flit, maturin) build a package from `pyproject.toml`.
- **Linter / formatter** — linters flag bugs and style issues (Ruff, flake8), formatters rewrite code to a canonical style (Black, Ruff format).
- **TUI (text/terminal user interface)** — full-screen terminal apps (Textual, prompt_toolkit), a step beyond line-based CLIs.
- **WebDriver** — the protocol Selenium uses to drive real browsers; Playwright uses its own driver model.
- **Notebook kernel** — the separate process executing notebook code (ipykernel for Python); the frontend (JupyterLab) just renders it.
- **Reactive notebook** — a notebook that re-runs dependent cells automatically when inputs change (Marimo), unlike Jupyter's manual execution order.
- **Pre-commit hook** — a script git runs before each commit (managed by the `pre-commit` tool) — typically linters and formatters.
- **C extension** — compiled C/C++/Rust code importable from Python (Cython generates it from Python-like syntax); how NumPy, orjson-class speed is achieved.
