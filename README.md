# PXU030 Portfolio Optimization

A research and visualization artifact for minimum-variance portfolio analysis associated with daily data covering **2020-01-01 through 2022-12-02**.

> **Research status:** this repository currently publishes a saved HTML analysis artifact. The complete end-to-end data and optimization workflow is not yet documented, so the artifact should not be treated as an independently reproducible benchmark or investment recommendation.

## Contents

| File | Description |
|---|---|
| [min-var.html](min-var.html) | Saved HTML artifact associated with the minimum-variance analysis; open it in a modern desktop browser |

## Scope

The project concerns portfolio optimization and visualization. Portfolio outputs can change materially with the selected instruments, return calculation, lookback window, constraints, missing-data handling, and transaction-cost assumptions.

This repository is an independent analytical demonstration. It is not investment advice, and an optimization result is not a promise of future performance.

## Reproducibility status

The current published material does not yet document all of the following:

- Original market-data source, instrument identifiers, frequency, and data license
- Data cleaning, corporate-action treatment, missing-value handling, and return calculation
- Objective function, constraints, estimation window, and optimizer settings
- Dependencies and a reproducible command that regenerates the HTML artifact
- Validation checks and out-of-sample analysis, including transaction-cost assumptions

These should be completed before reporting quantitative performance or presenting the result as evidence for a real-world allocation decision.

## Suggested environment

The repository currently centers on the saved HTML artifact. No complete installation or end-to-end regeneration procedure is claimed here until the original analysis code and dependencies are documented.

## Related projects

- [BIOGAS RS-PIM Engine](https://github.com/000MAK/biogas-rspim-engine)
- [Quantix — 100 Mini Python Projects](https://github.com/000MAK/quantix-100-new-mini-projects)
- [All public repositories](https://github.com/000MAK?tab=repositories)

## License and data

Check the repository's license files before reuse. Confirm the source and redistribution terms for any market data associated with the artifact; no market-data rights are implied by sharing the HTML file.
