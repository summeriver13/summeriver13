<div align="center">

# Xia Jiang

*I am, therefore I think.*

[![GitHub](https://img.shields.io/badge/-summeriver13-181717?logo=github&logoColor=white)](https://github.com/summeriver13)
[![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)](#)
[![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white)](#)

</div>

I work on developer tooling — the layer where a wrong answer from a linter or a build tool costs more than the code it checks.

## Background

| Period | What |
| --- | --- |
| 2026 – | M.Sc. in machine learning and big data, CCNU–UOW Joint Institute |
| 2024 – 2026 | Trading systems for A-share, HK, US and futures markets: CTP, Futu and QMT gateways, a C++ SDK wrapped into CPython, an Electron strategy terminal |
| 2024 | Access control and behaviour tracking for hospital operating rooms: face and IC-card identity, ISO 9001 / CE acceptance |
| 2020 – 2024 | B.Eng. in computer science |

Award: national bronze, China International "Internet+" College Students' Innovation and Entrepreneurship Competition.

## Upstream work

| Project | Change |
| --- | --- |
| [pylint-dev/pylint #11650](https://github.com/pylint-dev/pylint/pull/11650) | `pylint --source-root . pkg/mod` crashed when the package was an implicit namespace package that also exists in site-packages — merged, milestone 4.1.4 |
| [pylint-dev/pylint #11703](https://github.com/pylint-dev/pylint/pull/11703) | `--load-plugins` checkers emitted every message twice under `--jobs > 1` — merged, backported to `4.1.x` |
| [pylint-dev/astroid #3445](https://github.com/pylint-dev/astroid/pull/3445) | The astroid side of #11650: `is_namespace()` can take a search path, so a namespace package shadowed by site-packages is still recognized |
| [PyCQA/isort #2728](https://github.com/PyCQA/isort/pull/2728) | An action comment on a continuation line ends the sort section only on the next run |
| [python/cpython #160664](https://github.com/python/cpython/pull/160664) | `test_subprocess.test_getoutput` decoded `cmd.exe`'s OEM output as UTF-8, so it failed on every non-English Windows |

## Projects

| Repository | What it is |
| --- | --- |
| [summeriver13/plum](https://github.com/summeriver13/plum) | A-share backtesting and live trading, with the market's rules as first-class citizens: board-level price limits, T+1, halts, delisting settlement, participation-based market impact, point-in-time fundamentals |
| [summeriver13/herdface](https://github.com/summeriver13/herdface) | Cow face detection and identification: YOLOv8 for detection, EfficientNet-B0 for identity, open-set rejection at AUROC 0.912, Flask demo |
| [summeriver13/kt-audit](https://github.com/summeriver13/kt-audit) | Audit a knowledge-tracing evaluation before trusting its AUC |

## Toolchain

| Layer | Used |
| --- | --- |
| Backend | Python (Flask, FastAPI) · Go (Gin) · Ruby (Rails) · C++ |
| Frontend & desktop | React · Vue 3 · Next.js · Electron · PyQt6 |
| Infra & data | Docker · nginx · PostgreSQL · Redis · MongoDB · DuckDB · DolphinDB |
| Daily drivers | `uv` · `pnpm` · `ruff` · `biome` · `pytest` · `vitest` · `gh` |

<sub>Reproductions come first; a fix without a failing test is a guess.</sub>
