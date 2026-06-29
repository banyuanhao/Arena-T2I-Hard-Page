# Arena-T2I Hard — Project Page

Static project page for **Arena-T2I Hard: Benchmarking and Improving Faithfulness with a Dependency-Aware Checklist** (NeurIPS 2026, under double-blind review).

## What it covers

- **Arena-T2I Hard** — a 310-prompt stress benchmark of real arena user requests (~430 words, ~30 yes/no constraints per prompt) that stays discriminative where DPG-Bench and DSG saturate.
- **Dependency-aware checklist** — prompts are decomposed into a DAG of yes/no questions; failing a parent zeroes its descendants.
- **Reward–task mismatch & GDPO** — combining a checklist (faithfulness) reward with a Bradley-Terry (aesthetics) reward via group-decoupled normalization improves both axes on SD3.5-Medium and FLUX.1-dev.
- Leaderboard of 11 frontier closed-source systems and the main pairwise (MMRB2) results.

## Structure

- `index.html` — the entire page (content + layout).
- `static/css/index.css` — Bulma theme plus custom styles for the leaderboard, cards, and DAG example.
- `static/js/index.js` — copy-BibTeX, scroll-to-top, carousel/slider init.
- `static/images/` — figures sourced from the paper (`benchmark_comparison.png`, `training_curves_combined.png`, `matrix_sd3.png`, `matrix_flux.png`, `judge_eval.png`).

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Deploys as-is on GitHub Pages (`.nojekyll` is included).

## Before going public

Authors and affiliations are taken from the de-anonymized arXiv build. The following are still placeholders in `index.html`:

- The **Paper / arXiv / Code / Benchmark** buttons (`href="#"`).
- `og:url` meta tag (`https://YOUR_DOMAIN.com/arena-t2i-hard`).
- Optional per-author homepage links (names are currently plain text).

## Acknowledgments

Built on the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template), adopted from [Nerfies](https://nerfies.github.io). Licensed under CC BY-SA 4.0.
