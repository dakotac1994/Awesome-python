# Awesome Python

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Entries](https://img.shields.io/badge/entries-90-blue)](data/python.json)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

A curated list of the **Python ecosystem**: web frameworks, async networking, databases and ORMs, data science, machine learning, testing, packaging, linting and typing, CLIs and TUIs, web scraping, and developer tools.

> **Scope:** this list covers the *general-purpose Python ecosystem* — frameworks, libraries, and tools. LLM-specific Python tooling (LangChain, LlamaIndex, vLLM…) is out of scope here; it lives with the [Awesome-llms-labs](https://github.com/Awesome-llms-labs) family. Data science and core ML libraries (PyTorch, scikit-learn, Hugging Face transformers…) stay, since they are foundational Python.
> **Honesty policy:** every entry was checked against an official source (project repo, LICENSE file, or official site) as of 2026-09-30 — **90/90 verified**. Unverified entries carry a stated reason. Machine-readable data lives in [`data/python.json`](data/python.json).

## Contents

- [Web Frameworks](#web-frameworks) — 8 entries
- [Async & Networking](#async--networking) — 7 entries
- [Databases & ORMs](#databases--orms) — 7 entries
- [Task Queues & Scheduling](#task-queues--scheduling) — 6 entries
- [Data Science & Numerics](#data-science--numerics) — 8 entries
- [Machine Learning](#machine-learning) — 10 entries
- [Notebooks & Visualization](#notebooks--visualization) — 9 entries
- [Testing](#testing) — 6 entries
- [Packaging & Environments](#packaging--environments) — 7 entries
- [Linting, Formatting & Typing](#linting-formatting--typing) — 7 entries
- [CLI & TUI](#cli--tui) — 6 entries
- [Web Scraping & Automation](#web-scraping--automation) — 5 entries
- [Dev Tools](#dev-tools) — 4 entries

## Choosing the right Python library

New here? Start with the [choosing-a-python-library](docs/choosing-a-python-library.md) guide (maintenance signals, typing, performance, per-category picks), the [glossary](docs/glossary.md), and [status-changes](docs/status-changes.md) (renames, archival notices, license gotchas).

## Web Frameworks

Full-stack and API frameworks for building web applications and services, from batteries-included to minimalist ASGI. (8 entries)

- [Django](https://docs.djangoproject.com/) — High-level Python web framework with batteries-included ORM, auth, and admin interface. *(BSD-3-Clause · ⭐ 91,239)*
- [Falcon](https://falcon.readthedocs.io) — Minimalist WSGI/ASGI framework for building fast REST APIs and microservices. *(Apache-2.0 · ⭐ 9,806)*
- [FastAPI](https://fastapi.tiangolo.com/) — Modern ASGI web framework for building APIs with Python type hints and automatic OpenAPI docs. *(MIT · ⭐ 102,731)*
- [Flask](https://flask.palletsprojects.com) — Lightweight WSGI microframework for Python web applications and APIs. *(BSD-3-Clause · ⭐ 74,799)*
- [Litestar](https://docs.litestar.dev/) — ASGI web framework with first-class OpenAPI, dependency injection, and sync/async handlers. *(MIT · ⭐ 8,487)*
- [Quart](https://quart.palletsprojects.com) — Asyncio reimplementation of the Flask API for building async web applications. *(MIT · ⭐ 3,674)*
- [Sanic](https://sanic.dev) — Async Python web framework built for high-throughput HTTP services. *(MIT · ⭐ 18,638)*
- [Tornado](https://www.tornadoweb.org/) — Python web framework and asynchronous networking library with non-blocking I/O. *(Apache-2.0 · ⭐ 22,178)*

## Async & Networking

Async I/O primitives, HTTP clients, and servers for concurrent Python. (7 entries)

- [aiohttp](https://docs.aiohttp.org) — Asyncio-based HTTP client and server framework for Python. *(Apache-2.0 · ⭐ 16,567)*
- [anyio](https://anyio.readthedocs.io/en/stable/) — Compatibility layer letting async code run unmodified on either asyncio or trio. *(MIT · ⭐ 2,550)*
- [gunicorn](https://www.gunicorn.org) — Pre-fork worker model WSGI HTTP server for running Python web applications. *(MIT · ⭐ 10,688)*
- [httpx](https://www.python-httpx.org/) — Full-featured HTTP client with sync and async APIs and HTTP/1.1 and HTTP/2 support. *(BSD-3-Clause · ⭐ 15,524)*
- [trio](https://trio.readthedocs.io) — Structured-concurrency async I/O library offering an alternative programming model to asyncio. *(MIT OR Apache-2.0 · ⭐ 7,342)*
- [uvicorn](https://uvicorn.dev) — Lightning-fast ASGI server implementation for running Python web apps. *(BSD-3-Clause · ⭐ 11,000)*
- [websockets](https://websockets.readthedocs.io/) — Library for building WebSocket servers and clients in asyncio applications. *(BSD-3-Clause · ⭐ 5,721)*

## Databases & ORMs

SQL toolkits, ORMs, drivers, and migration tools for talking to databases. (7 entries)

- [alembic](https://alembic.sqlalchemy.org/en/latest/) — Database migration tool for SQLAlchemy with autogenerate support. *(MIT · ⭐ 4,424)*
- [asyncpg](https://magicstack.github.io/asyncpg/current/) — Fast asyncio PostgreSQL driver using the native binary protocol. *(Apache-2.0 · ⭐ 8,096)*
- [Peewee](https://docs.peewee-orm.com/) — Small, expressive ORM supporting SQLite, MySQL, and PostgreSQL. *(MIT · ⭐ 11,996)*
- [Piccolo](https://piccolo-orm.com/) — Async-friendly ORM and query builder with built-in migrations and admin UI. *(MIT · ⭐ 1,948)*
- [psycopg](https://www.psycopg.org/psycopg3/) — PostgreSQL adapter for Python 3 with both sync and async DB-API and raw interfaces. *(LGPL-3.0 · ⭐ 2,503)*
- [SQLAlchemy](https://docs.sqlalchemy.org/) — SQL toolkit and ORM for Python with support for many database backends. *(MIT · ⭐ 12,192)*
- [Tortoise ORM](https://tortoise.github.io) — Async ORM for Python inspired by Django's ORM, with Pydantic integration. *(Apache-2.0 · ⭐ 5,634)*

## Task Queues & Scheduling

Background job processing and scheduled task execution. (6 entries)

- [APScheduler](https://apscheduler.readthedocs.io/) — In-process task scheduler with cron-like, interval, and one-off triggers. *(MIT · ⭐ 7,643)*
- [arq](https://arq-docs.helpmanual.io/) — Fast asyncio job queue for Python built on Redis. *(MIT · ⭐ 3,013)*
- [Celery](https://docs.celeryq.dev) — Distributed task queue for Python, commonly backed by Redis or RabbitMQ. *(BSD-3-Clause · ⭐ 28,928)*
- [Dramatiq](https://dramatiq.io) — Fast, reliable background task processing library with actor-model semantics. *(LGPL-3.0 · ⭐ 5,318)*
- [Huey](https://huey.readthedocs.io/) — Small multi-purpose task queue backed by Redis, SQLite, or in-memory storage. *(MIT · ⭐ 6,041)*
- [RQ](https://python-rq.org) — Simple Redis-backed job queue for Python with a minimal API. *(BSD-2-Clause · ⭐ 10,695)*

## Data Science & Numerics

Arrays, DataFrames, and scientific computing: the numerical Python stack. (8 entries)

- [Dask](https://docs.dask.org/en/stable/) — Parallel computing library for scaling NumPy, pandas, and scikit-learn workloads via task graphs and distributed schedulers. *(BSD-3-Clause · ⭐ 13,927)*
- [Numba](https://numba.readthedocs.io/en/stable/) — JIT compiler translating Python and NumPy code to optimized machine code via LLVM for fast numerical computing. *(BSD-2-Clause · ⭐ 11,169)*
- [NumPy](https://numpy.org/doc/) — Fundamental package for scientific computing with n-dimensional arrays, vectorized math, and linear algebra routines. *(BSD-3-Clause · ⭐ 32,887)*
- [pandas](https://pandas.pydata.org/docs/) — Data analysis library providing labeled DataFrame/Series structures and fast data manipulation; 3.x era in 2026 alongside Polars momentum. *(BSD-3-Clause · ⭐ 49,883)*
- [Polars](https://docs.pola.rs) — Blazing-fast DataFrame library written in Rust with a Python API, built on Apache Arrow memory; the modern challenger to pandas. *(MIT · ⭐ 39,899)*
- [PyArrow](https://arrow.apache.org/docs/python/) — Python bindings for Apache Arrow: in-memory columnar format, Parquet/Feather I/O, and zero-copy data interchange between tools. *(Apache-2.0 · ⭐ 17,166)*
- [SciPy](https://docs.scipy.org/doc/scipy/) — Library for scientific and technical computing: optimization, integration, interpolation, signal/image processing, statistics. *(BSD-3-Clause · ⭐ 15,060)*
- [xarray](https://docs.xarray.dev/en/stable/) — N-dimensional labeled arrays and datasets for working with NetCDF, GRIB, Zarr and other multidimensional scientific data. *(Apache-2.0 · ⭐ 4,206)*

## Machine Learning

Classical ML, deep learning frameworks, gradient boosting, and the core Hugging Face libraries. (10 entries)

- [datasets](https://huggingface.co/docs/datasets) — Library for loading, sharing, and processing datasets for AI models, with fast Arrow-backed data manipulation tools. *(Apache-2.0 · ⭐ 22,021)*
- [JAX](https://docs.jax.dev) — Composable transformations of NumPy programs: automatic differentiation, vectorization, and JIT compilation to GPU/TPU. *(Apache-2.0 · ⭐ 36,367)*
- [LightGBM](https://lightgbm.readthedocs.io/en/latest/) — Fast distributed gradient boosting framework based on decision trees; repo moved from microsoft/LightGBM to lightgbm-org/LightGBM. *(MIT · ⭐ 18,824)*
- [Optuna](https://optuna.readthedocs.io/en/stable/) — Automatic hyperparameter optimization framework using define-by-run search spaces and efficient sampling/pruning algorithms. *(MIT · ⭐ 14,865)*
- [PyTorch](https://docs.pytorch.org/docs/stable/index.html) — Deep learning framework with dynamic computation graphs, strong GPU acceleration, and the dominant research ecosystem in 2026. *(BSD-3-Clause · ⭐ 103,571)*
- [scikit-learn](https://scikit-learn.org/stable/) — Machine learning in Python: classical algorithms for classification, regression, clustering, plus preprocessing and model selection. *(BSD-3-Clause · ⭐ 67,435)*
- [TensorFlow](https://www.tensorflow.org/api_docs) — Google's deep learning framework (Keras is the recommended high-level API); actively maintained with a strong production/serving ecosystem. *(Apache-2.0 · ⭐ 200,645)*
- [tokenizers](https://huggingface.co/docs/tokenizers) — Fast tokenizers for NLP research and production, implemented in Rust with Python bindings; powers the transformers library. *(Apache-2.0 · ⭐ 11,144)*
- [transformers](https://huggingface.co/docs/transformers) — Hugging Face library providing pretrained model definitions and pipelines for text, vision, audio, and multimodal models. *(Apache-2.0 · ⭐ 166,872)*
- [XGBoost](https://xgboost.readthedocs.io/) — Optimized distributed gradient boosting (GBDT/GBM) library with Python, R, and JVM bindings; still a tabular-data workhorse. *(Apache-2.0 · ⭐ 28,809)*

## Notebooks & Visualization

Interactive notebooks and plotting libraries, from static figures to reactive apps. (9 entries)

- [Altair](https://altair-viz.github.io/) — Declarative statistical visualization library based on the Vega-Lite grammar of interactive graphics. *(BSD-3-Clause · ⭐ 10,488)*
- [Bokeh](https://docs.bokeh.org/en/latest/) — Interactive visualization library for modern browsers; actively developed (3.10.0 released, 4.0 branch in progress as of late 2026). *(BSD-3-Clause · ⭐ 20,460)*
- [ipywidgets](https://ipywidgets.readthedocs.io) — Interactive HTML widgets for Jupyter notebooks and kernels: sliders, buttons, plots, and custom widget authoring. *(BSD-3-Clause · ⭐ 3,332)*
- [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/) — The classic interactive notebook UI; v7 is built on JupyterLab components (the legacy 6.5.x branch is maintenance/security only). *(BSD-3-Clause · ⭐ 13,407)*
- [JupyterLab](https://jupyterlab.readthedocs.io/) — The primary current Jupyter computational environment: extensible web-based IDE with notebooks, terminals, and file browsers. *(BSD-3-Clause · ⭐ 15,327)*
- [Marimo](https://docs.marimo.io/) — Reactive Python notebook stored as plain .py files: reproducible, executable as scripts, deployable as apps, git-friendly. *(Apache-2.0 · ⭐ 22,958)*
- [Matplotlib](https://matplotlib.org/stable/) — Comprehensive 2D/3D plotting library; the foundational static-plot backend underlying most Python visualization. *(Matplotlib (BSD-compatible) · ⭐ 23,310)*
- [Plotly](https://plotly.com/python/) — Interactive graphing library producing browser-based charts and dashboards, with tight integration for Dash apps. *(MIT · ⭐ 18,817)*
- [Seaborn](https://seaborn.pydata.org/) — Statistical data visualization built on Matplotlib, with a high-level interface for attractive informative plots. *(BSD-3-Clause · ⭐ 14,052)*

## Testing

Test runners, property-based testing, coverage measurement, and test automation. (6 entries)

- [coverage.py](https://coverage.readthedocs.io) — Measures code coverage of Python programs and reports which lines ran. *(Apache-2.0 · ⭐ 3,410)*
- [Hypothesis](https://hypothesis.readthedocs.io) — Property-based testing: generates random test cases and shrinks failures to minimal reproductions. *(MPL-2.0 · ⭐ 9,032)*
- [nox](https://nox.thea.codes) — Test automation across multiple Python versions, configured in plain Python files. *(Apache-2.0 · ⭐ 1,561)*
- [pytest](https://docs.pytest.org) — Mature, full-featured testing framework with fixtures, parametrization, and a large plugin ecosystem. *(MIT · ⭐ 14,556)*
- [pytest-xdist](https://pytest-xdist.readthedocs.io) — pytest plugin for parallel and distributed test execution. *(MIT · ⭐ 1,913)*
- [tox](https://tox.wiki) — Automates testing across multiple Python versions and isolated environments. *(MIT · ⭐ 3,942)*

## Packaging & Environments

Installers, environment managers, and project/packaging workflows. (7 entries)

- [conda](https://docs.conda.io) — Cross-language package and environment manager; conda-forge is the community package channel. *(BSD-3-Clause · ⭐ 7,522)*
- [Hatch](https://hatch.pypa.io) — Modern project manager and PEP 517 build backend (hatchling) from the PyPA. *(MIT · ⭐ 7,242)*
- [PDM](https://pdm-project.org) — Modern package manager with PEP 582 local packages and lockfile support. *(MIT · ⭐ 8,667)*
- [pip](https://pip.pypa.io) — The reference Python package installer, bundled with CPython. *(MIT · ⭐ 10,290)*
- [Poetry](https://python-poetry.org/docs) — Dependency management and packaging with lockfiles, build, and publish support. *(MIT · ⭐ 34,306)*
- [uv](https://docs.astral.sh/uv) — Extremely fast Python package and project manager in Rust, with lockfiles and managed Python installs. *(Apache-2.0 OR MIT · ⭐ 90,322)*
- [virtualenv](https://virtualenv.pypa.io) — Creates isolated Python environments. *(MIT · ⭐ 5,050)*

## Linting, Formatting & Typing

Linters, formatters, and static type checkers — plus runtime data validation. (7 entries)

- [Black](https://black.readthedocs.io) — The uncompromising Python code formatter. *(MIT · ⭐ 41,857)*
- [flake8](https://flake8.pycqa.org) — Style, error, and complexity checker combining pyflakes, pycodestyle, and McCabe. *(MIT · ⭐ 3,826)*
- [isort](https://pycqa.github.io/isort) — Sorts imports into sections and alphabetical order. *(MIT · ⭐ 6,959)*
- [mypy](https://mypy.readthedocs.io) — Static type checker for Python (mypyc, its optimizing compiler, ships in the same repo). *(MIT · ⭐ 20,652)*
- [pydantic](https://docs.pydantic.dev) — Data validation and settings management driven by type annotations. *(MIT · ⭐ 28,909)*
- [pyright](https://microsoft.github.io/pyright) — Static type checker for Python written in TypeScript, by Microsoft. *(MIT · ⭐ 15,669)*
- [Ruff](https://docs.astral.sh/ruff) — Extremely fast linter and formatter in Rust (covers flake8/isort-style rules plus its own formatter). *(MIT · ⭐ 49,861)*

## CLI & TUI

Command-line interface builders and full-screen terminal UI frameworks. (6 entries)

- [Click](https://click.palletsprojects.com) — Composable toolkit for building command-line interfaces. *(BSD-3-Clause · ⭐ 17,780)*
- [Fire](https://google.github.io/python-fire) — Turns any Python object into a command-line interface automatically. *(Apache-2.0 · ⭐ 28,226)*
- [prompt_toolkit](https://python-prompt-toolkit.readthedocs.io) — Building blocks for interactive CLI prompts, REPLs, and full-screen terminal apps. *(BSD-3-Clause · ⭐ 10,592)*
- [Rich](https://rich.readthedocs.io) — Terminal rendering: tables, progress bars, syntax highlighting, markdown. *(MIT · ⭐ 57,457)*
- [Textual](https://textual.textualize.io) — Framework for full-screen terminal applications, from the Rich author. *(MIT · ⭐ 37,374)*
- [Typer](https://typer.tiangolo.com) — Build CLIs from type hints, built on Click. *(MIT · ⭐ 20,045)*

## Web Scraping & Automation

HTML parsing, crawling frameworks, and real-browser automation. (5 entries)

- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) — HTML/XML parsing library for extracting data from web pages. *(MIT)*
- [MechanicalSoup](https://mechanicalsoup.readthedocs.io) — Automates website interaction (forms, links) on top of requests and BeautifulSoup. *(MIT · ⭐ 4,898)*
- [Playwright](https://playwright.dev/python) — Python client for Playwright: script real browsers for testing and scraping. *(Apache-2.0 · ⭐ 15,021)*
- [Scrapy](https://docs.scrapy.org) — High-level web crawling and scraping framework. *(BSD-3-Clause · ⭐ 64,537)*
- [Selenium](https://www.selenium.dev/documentation/) — Browser automation via WebDriver; the Python package drives real browsers. *(Apache-2.0 · ⭐ 34,525)*

## Dev Tools

Project scaffolding, git hooks, app distribution, and C-extension compilation. (4 entries)

- [cookiecutter](https://cookiecutter.readthedocs.io) — Project scaffolding from templates ("cookiecutters"). *(BSD-3-Clause · ⭐ 25,120)*
- [Cython](https://cython.readthedocs.io) — Compiles Python-like code to C extensions for C-level speed. *(Apache-2.0 · ⭐ 10,853)*
- [pipx](https://pipx.pypa.io) — Installs and runs Python CLI apps in isolated environments. *(MIT · ⭐ 12,976)*
- [pre-commit](https://pre-commit.com) — Manages and runs git pre-commit hooks across repos and languages. *(MIT · ⭐ 15,603)*

## Notable exclusions

Candidates that were researched and deliberately left out:

| Excluded | Reason |
| --- | --- |
| nose | Dead: last release 2015; superseded by pytest (listed). |
| requests-html | Dormant since 2019; effectively unmaintained. |
| Theano | Development ended 2017. |
| Caffe | Archived/dead upstream. |
| Bocadillo / Responder | Once-promising ASGI frameworks; effectively unmaintained. |
| Django Q (`Koed00/django-q`) | No commits since 2024-08; superseded by the community fork django-q2. |
| LangChain / LlamaIndex / Haystack | LLM-specific frameworks — out of scope; see the Awesome-llms-labs org. |
| vLLM / TRL / PEFT / Diffusers / Sentence Transformers | LLM-specific tooling — out of scope; see the Awesome-llms-labs org. |
| `microsoft/LightGBM` (old path) | Repo moved to `lightgbm-org/LightGBM` (listed); the old path 301-redirects. |
| Keras (standalone) | Keras 3 is the high-level API inside TensorFlow/JAX/PyTorch; covered by the TensorFlow entry. |
| TorchVision / TorchText / TorchAudio | Sub-packages of the PyTorch ecosystem; covered by the PyTorch entry. |
| starlette | ASGI toolkit and FastAPI's foundation, but a building block rather than a full framework. |
| gevent / eventlet | Greenlet-based concurrency; outside this list's asyncio-focused async scope. |
| curio | Structured-concurrency pioneer, superseded by trio/anyio (listed). |

## Related

More curated lists by the same author:

- [Awesome-terminal](https://github.com/dakotac1994/Awesome-terminal) — terminal emulators and the terminal stack..
- [Awesome-diagram-tool](https://github.com/dakotac1994/Awesome-diagram-tool) — diagramming and visualization tools..
- [Awesome-chrome-extension](https://github.com/dakotac1994/Awesome-chrome-extension) — Chrome/Chromium browser extensions..
- [Awesome-db](https://github.com/dakotac1994/Awesome-db) — database engines by data model..
- [awesome-cli](https://github.com/dakotac1994/awesome-cli) — the broad CLI/TUI tools list..
- [awesome-oss-cli](https://github.com/dakotac1994/awesome-oss-cli) — the OSS-only CLI/TUI list..
- [awesome-oss-macos](https://github.com/Awesome-llms-labs/awesome-oss-macos) — open-source macOS apps..

LLM-specific Python tooling lives with the [Awesome-llms-labs](https://github.com/Awesome-llms-labs) organization.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome — every entry must be verified against an official source, with the license copied from the project's actual LICENSE file.
