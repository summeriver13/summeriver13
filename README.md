<div align="center">

# Xia Jiang

[![GitHub](https://img.shields.io/badge/-summeriver13-181717?logo=github&logoColor=white)](https://github.com/summeriver13)
[![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![kt-audit](https://img.shields.io/pypi/v/kt-audit?label=kt-audit)](https://pypi.org/project/kt-audit/)

</div>

M.Sc. student in Machine Learning and Big Data at CCNU–UOW. I work on knowledge tracing, quantitative trading systems, and upstream developer tooling — linters, runtimes, and locale data. A wrong answer there is silent and expensive.

## Currently

Auditing KT evaluation in **kt-audit**; upstream work on pylint, astroid, and CPython; open to ML-infra and quant-trading internships.

## Education

- **2026–2028 (expected)** M.Sc. in Machine Learning and Big Data, CCNU–UOW Joint Institute
- **2020–2024** B.Eng. in Computer Science and Technology, Inner Mongolia University of Technology

## Experience

- **2024–2026** Trading systems for A-share, HK, US, and futures markets: CTP, Futu, and QMT gateways, a C++ SDK wrapped into CPython, and an Electron strategy terminal
- **2024** Access control and identity verification for a clinical operating-room (OR) environment (details withheld)

## Upstream work

| Project | Change | Status | Last checked |
| --- | --- | --- | --- |
| [pylint-dev/pylint #11650](https://github.com/pylint-dev/pylint/pull/11650) | Fixed a crash when a namespace package also exists in site-packages. | Merged · shipped in 4.1.4 | 2026-11 |
| [pylint-dev/pylint #11703](https://github.com/pylint-dev/pylint/pull/11703) | Fixed duplicate messages from `--load-plugins` checkers with `--jobs > 1`. | Merged · backported to 4.1.x | 2026-11 |
| [pylint-dev/astroid #3445](https://github.com/pylint-dev/astroid/pull/3445) | Added an optional search path to `is_namespace()` so a namespace package shadowed by site-packages is still recognized. | In review | 2026-11 |
| [PyCQA/isort #2728](https://github.com/PyCQA/isort/pull/2728) | Fixed action comments on continuation lines ending a sort section only on the next run. | Changes requested; merge conflict | 2026-11 |
| [python/cpython #160664](https://github.com/python/cpython/pull/160664) | Fixed `test_subprocess.test_getoutput` decoding `cmd.exe` OEM output as UTF-8 on non-English Windows. | Approved, pending merge | 2026-11 |
| [python/cpython #160716](https://github.com/python/cpython/pull/160716) | Fixed the remote PDB interrupt listener half-closing its socket on Windows. | Approved, pending merge | 2026-11 |
| [python-babel/babel #1383](https://github.com/python-babel/babel/pull/1383) | Added CLDR 49 `ddd` ordinal day-of-month patterns; fixes ordinal suffixes in locales using `ddd`. | Approved, pending CI and merge | 2026-11 |

**Docs / community:** [ruby/TryRuby #258](https://github.com/ruby/TryRuby/pull/258) — Chinese translation fixes for lessons 1–20 (in review).

## Projects

### [kt-audit](https://github.com/summeriver13/kt-audit)

[![PyPI](https://img.shields.io/pypi/v/kt-audit)](https://pypi.org/project/kt-audit/)
[![CI](https://github.com/summeriver13/kt-audit/actions/workflows/ci.yml/badge.svg)](https://github.com/summeriver13/kt-audit/actions/workflows/ci.yml)
[![Python](https://img.shields.io/pypi/pyversions/kt-audit)](https://pypi.org/project/kt-audit/)

Audit knowledge-tracing evaluation before you trust the AUC. It checks temporal leakage, item and KC overlap, prediction alignment, and metric recomputation. `pip install kt-audit`; status: alpha (0.3.x).

In pyKT, preprocessing is version-dependent: [v0.0.38](https://github.com/pykt-team/pykt-toolkit/blob/v0.0.38/pykt/preprocess/data_proprocess.py) uses `pykt/preprocess/data_proprocess.py`, while [v1.0.0](https://github.com/pykt-team/pykt-toolkit/blob/v1.0.0/examples/data_preprocess.py) uses `examples/data_preprocess.py`. kt-audit checks the release you actually run before you cite its number.

### [plum](https://github.com/summeriver13/plum)

A-share backtesting and live trading where the market's rules live in the engine, not in the strategy. Board-level price limits (20% on ChiNext and STAR; 5% on main-board ST), T+1 settlement, halts, delisting settlement at the last close, square-root market impact capped by participation, and point-in-time fundamentals. Cash and the ledger use `Decimal`, so the book never drifts on float error.

## Toolchain

| Level | Tools |
| --- | --- |
| Primary | Python · C++ · pytest · uv · ruff · CPython tooling |
| Familiar | Go · Ruby/Rails · React/Vue · Next.js · Electron · PyQt6 · PostgreSQL · Redis · DuckDB · DolphinDB |
| Daily drivers | `uv` · `pnpm` · `ruff` · `biome` · `pytest` · `vitest` · `gh` |

<sub>*I am, therefore I think.* · Reproductions come first; a fix without a failing test is a guess.</sub>
