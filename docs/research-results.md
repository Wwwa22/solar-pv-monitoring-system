# Research results and evidence scope

This page summarizes aggregate findings from two private manuscripts supplied by Saeed Ali Asiri and reviewed on **16 October 2026**. It publishes neither the manuscripts nor their methods, figures, datasets, or implementation.

## 1. Forecasting study

**Research objective:** prototype-scale PV power forecasting combining physical modelling and machine learning. Seven-day forecasting is the manuscript's stated objective.

### Evaluation context

| Item | Reported scope |
| --- | --- |
| Evaluated records | 12,834 rows |
| Training records | 10,267 rows |
| Test records | 2,567 rows |
| Split described by the manuscript | Source-time holdout |
| Output assessed | PV power |
| Reported measures | MAE, RMSE, and R² |
| Validation scale | One prototype-scale dataset |

The sample counts describe evaluation scope; no records or dataset download are provided.

### Reported performance

Values below were checked against **Table II on page 2 of the forecasting manuscript**.

| Approach | MAE (W) | RMSE (W) | R² |
| --- | ---: | ---: | ---: |
| Physical-model baseline | 1.878 | 3.111 | 0.953 |
| Best evaluated hybrid forecast | 0.824 | 1.615 | 0.987 |

The hybrid has lower reported MAE and RMSE than the baseline on this evaluation. Its relative MAE reduction is approximately **56.1%** and its relative RMSE reduction is approximately **48.1%**, computed as the decrease divided by the corresponding baseline value, using the rounded values in the table.

R² is a regression goodness-of-fit measure. **R² = 0.987 is not a claim of 98.7% classification accuracy.**

Algorithm selection, feature construction, equations, model settings, and training procedures are intentionally omitted from this public summary.

### What the evidence establishes

The supplied manuscript reports a quantitative improvement over its physical baseline for the evaluated prototype dataset and split. This supports describing the work as forecasting research with documented numerical results.

### What remains unverified

The benchmark has not been independently reproduced from raw data and executable evaluation code. The supplied manuscript does not provide per-lead-time scores, uncertainty intervals, or multi-site validation. Its aggregate metrics therefore do not establish the same performance on every day of a seven-day horizon or on another PV installation.

The monitoring source repository was inspected separately. The research score must not be attributed to its existing display estimate or treated as proof of a deployed trained model.

## 2. Weather-aware monitoring study

**Research objective:** use PV monitoring and weather context to identify underperformance requiring further inspection.

The following single prototype case was checked against **Table II and the accompanying case discussion on page 2 of the monitoring manuscript**.

| Case quantity | Reported value |
| --- | ---: |
| Predicted / baseline power | 20.52 W |
| Measured live power | 0.00 W |
| Reported power error | -20.52 W |
| Cloud cover | 40% |
| Alert severity | High |

The case illustrates a large mismatch between expected and measured output. The manuscript treats the alert as a reason to inspect; it does not confirm a particular physical cause.

This is one reported case, not a detection benchmark. It does not establish precision, recall, false-alarm rate, sensor accuracy, or calibrated fault diagnosis. The alert decision logic and operating thresholds are not disclosed.

## 3. Evidence and publication status

- **Evidence reviewed:** two author-provided private manuscripts; relevant tables and narrative were checked visually and by text extraction.
- **Public disclosure:** aggregate metrics, a single reported case, high-level purpose, and evaluation context.
- **Independent reproduction:** not performed.
- **Deployment:** not established by the manuscripts.
- **Publication status:** no conference acceptance, published DOI, or peer-review status has been established by these files.
- **IP:** no patent-grant claim or patent-sensitive implementation is disclosed.

No paper download, internal file link, manuscript screenshot, dataset, source code, or detailed method is included in this repository.

[Back to the showcase](../README.md)
