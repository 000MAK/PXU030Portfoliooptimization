# PXU030 Portfolio Optimization

A research and visualization artifact for minimum-variance portfolio analysis associated with daily data covering **2020-01-01 through 2022-12-02**.

> **Research status:** a 2022 coursework-style analysis. The R Markdown source and its rendered HTML are both published; rerunning it downloads current Yahoo Finance data, so numbers will differ from the saved HTML. Not a benchmark or investment recommendation.

## Contents

| File | Description |
|---|---|
| [min-var.Rmd](min-var.Rmd) | R Markdown source of the analysis, reconstructed from the code shown in the HTML (it was knitted with `echo = TRUE`, so every code chunk is preserved verbatim) |
| [min-var.html](min-var.html) | Rendered output from 2022-11-18 (11.8 MB, too large for GitHub's preview; download and open it in a desktop browser) |

## Method

- **Universe:** 30 large-cap Borsa Istanbul stocks (AKBNK, AKSEN, ARCLK, ASELS, BIMAS … YKBNK).
- **Data:** daily prices from Yahoo Finance via `tidyquant`/`quantmod`, from 2020-01-01; daily simple returns; annualised with 252 trading days. (A code comment mentions month-end prices, but the code uses daily data.)
- **Optimisation:** Monte Carlo search over 50,000 random long-only, fully invested weight vectors; the minimum-variance and maximum-Sharpe portfolios are picked from the sample. The Sharpe ratio uses no risk-free rate.
- **Caveats:** random search approximates, but does not exactly solve, the minimum-variance problem; there is no out-of-sample test, transaction costs or rebalancing.

To rerun: open `min-var.Rmd` in RStudio with `tibble`, `tidyr`, `tidyquant`, `plotly`, `timetk`, `forcats`, `PerformanceAnalytics` and `ggplot2` installed, and knit.

## Scope

The project concerns portfolio optimization and visualization. Portfolio outputs can change materially with the selected instruments, return calculation, lookback window, constraints, missing-data handling, and transaction-cost assumptions.

This repository is an independent analytical demonstration. It is not investment advice, and an optimization result is not a promise of future performance.

## Reproducibility status

Documented now: data source, universe, return calculation, objective, constraints and the full code. Still missing:

- Yahoo Finance terms and a frozen copy of the price data (rerunning fetches today's data)
- Corporate-action and missing-value handling beyond `na.omit()`
- An exact optimiser (e.g. quadratic programming) to compare with the random search
- Out-of-sample evaluation and transaction-cost assumptions

These should be completed before reporting quantitative performance or presenting the result as evidence for a real-world allocation decision.

## Suggested next steps

1. Document the data source, column schema, frequency, and license.
2. Add source code and an environment file that reproduce the artifact from permitted data.
3. Include a small synthetic example and tests for the optimization constraints.
4. Report assumptions, baseline comparisons, and appropriately scoped out-of-sample evaluation.

## Related projects

- [BIOGAS RS-PIM Engine](https://github.com/000MAK/biogas-rspim-engine)
- [Quantix — 100 Mini Python Projects](https://github.com/000MAK/quantix-100-new-mini-projects)
- [All public repositories](https://github.com/000MAK?tab=repositories)

## License and data

At the time this README was updated, no LICENSE file was found in this repository. Without an explicit license, public visibility does not by itself grant permission to reuse or redistribute the project. Add a license if you intend to permit reuse, and document the source and redistribution terms for any market data associated with the artifact.
