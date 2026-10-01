# Status Changes

Notable renames, archival notices, dormancy, and license gotchas affecting entries in this list. Last reviewed 2026-09-30.

## Renames / moves

- **LightGBM: `microsoft/LightGBM` → `lightgbm-org/LightGBM`** — the repo moved orgs; the old path 301-redirects. Entries use the canonical new path.
- **python-httpx.org → httpx.sh** — the httpx docs domain moved; entries link the current canonical docs.
- **Jupyter Notebook v7** — the classic Notebook UI is now built on JupyterLab components; the 6.5.x line is maintenance-only. JupyterLab is the primary current environment; both are listed as distinct entries.

## Maintenance notes (verified 2026-09-30)

- **Celery is NOT dormant** — v5.6.3 released 2026-03-26, commits landing on main; abandonment rumors are stale.
- **Peewee is active** — v4.5.2 released 2026-09-27.
- **Tornado / Sanic / Falcon all active** — Falcon 4.4.0 released 2026-09-30; Tornado and Sanic both pushed in 2026.
- **httpx is in stable maintenance mode** — last release Dec 2024, last commit Mar 2026. Normal for a mature client library, not a dormancy signal.
- **arq is slow-moving but maintained** — v0.28.0 (Apr 2026); kept as the asyncio-native queue option.
- **APScheduler's maintained line is 3.11.x** — the 4.x rewrite has been pending for years; entries reference the 3.x line.
- **Bokeh is active** — 3.10.0 released, 4.0 branch in progress (contrary to occasional "dead" claims).
- **Dask is active** — pushed 2026-09-29, not archived.

## License gotchas (verified on official sources)

- **Matplotlib** — recorded as `Matplotlib (BSD-compatible)`: the actual LICENSE file is the "License agreement for matplotlib versions 1.3.0 and later" (BSD-style, PSF-derived), and GitHub reports no SPDX identifier. Not invented as BSD-3-Clause.
- **trio** — dual-licensed `MIT OR Apache-2.0`.
- **uv** — dual-licensed `Apache-2.0 OR MIT`.
- **dramatiq / psycopg** — **LGPL-3.0** (not MIT/Apache; read from the LICENSE files).
- **RQ** — **BSD-2-Clause** (no endorsement clause), not BSD-3-Clause.
- **gunicorn** — MIT (GitHub's API reports NOASSERTION; the LICENSE file is MIT text).
- **PyTorch** — BSD-3-Clause (GitHub's API reports NOASSERTION; the LICENSE file is BSD-3-clause text).
- **Hypothesis** — **MPL-2.0** (not MIT).

## Excluded on purpose

- **nose / nose2** — nose is dead (2015); nose2 is maintained but redundant next to pytest.
- **requests-html** — dormant since 2019.
- **Theano / Caffe** — dead upstream.
- **LLM-specific Python tooling** (LangChain, LlamaIndex, vLLM, TRL, PEFT, Diffusers, Sentence Transformers…) — out of scope; belongs to the Awesome-llms-labs org family.
