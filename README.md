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
