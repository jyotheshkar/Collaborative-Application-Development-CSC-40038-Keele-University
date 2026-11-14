# Collaborative Application Development

Conference booking analysis and forecasting, developed as a team project during my MSc Computer Science at Keele University in **2023/24**. The repository contains Python analysis, imputation and model experiments, a Tkinter prediction interface, and a preserved history of my exploratory data-analysis scripts.

| Academic record | Detail |
| --- | --- |
| Module | Collaborative Application Development, CSC-40038 |
| Level and credit | Level 7, 15 CATS |
| Verified module mark | **77%** |
| Project year | **2024** |

The mark is the overall module result, verified against my private official transcript; it is not an application accuracy or a separate component mark. [Keele's archived 2023/24 specification](https://www.keele.ac.uk/catalogue/2023-24/csc-40038.htm) describes the team development, client presentation and reflective assessment context.

## What the project does

The team investigated seven conference datasets, analysed booking patterns, compared regression, classification and time-series approaches, and explored missing-data imputation. The delivered desktop interface accepts an event's dates, current bookings and target audience, then calls the selected prediction code. It is academic software rather than a packaged desktop release.

My [professional contribution excerpt](docs/original/personal-contribution-excerpt.md) records my work developing Python booking-analysis scripts, comparing results with a teammate's Excel analysis, and attempting a React/Flask prototype before the team moved to a Tkinter interface. The React/Flask source is not present here. The model comparison, imputation research and final solution were shared team work; this portfolio does not claim sole authorship of them.

## Explore the evidence

| Material | What to inspect |
| --- | --- |
| [Data Analysis](Data%20Analysis/dataAnalysis.py) | Weekly counts, z-scores, plots and Excel reports |
| [Prediction Model and GUI](Prediction%20Model%20and%20GUI) | Event manifest, audience aggregation, ElasticNet forecasting and Tkinter interface |
| [Regression Models](Regression%20Models), [Classification Models](Classification%20Models), [Time Series Models](Time%20Series%20Models) | Historical model experiments, with their original assumptions |
| [Data Imputation](Data%20Imputation) | Missing-data experiments |
| [Original data-analysis history](original-work/Data-Analytics) | Earlier iterations preserved with an import provenance manifest |
| [Coursework walkthrough](docs/COURSEWORK.md) | Skills connected to actual source and contribution boundaries |
| [Assignment evidence](docs/original/README.md) | Official reflection brief and privacy-reviewed student-report extracts |

## Run locally

Download or clone the complete repository, then use a virtual environment with Python 3.12. Install Tk support through your Python distribution if it is not included.

```bash
python -m venv .venv
```

Activate it with `.venv\Scripts\Activate.ps1` on Windows PowerShell, or `source .venv/bin/activate` on macOS/Linux. Then:

```bash
python -m pip install -r requirements-maintenance.txt
python -m unittest discover -s tests -v
cd "Prediction Model and GUI"
python GUI.py
```

Running from that directory also supports historical scripts that use relative filenames. The maintained data-preparation and attendance-data imports resolve their inputs beside the source file. See [engineering notes](docs/ENGINEERING.md) for dependencies needed by exploratory plots, output locations and evaluation limits.

The existing `web/` directory is a separate **2026 synthetic teaching illustration**. It does not execute the Python prediction models, use these event datasets or reproduce the 2024 assessment. It is not evidence of a deployed forecasting service.

## Validation and limitations

The preparation regression loads all seven event files from an unrelated working directory and checks event pairing, date types, removal of post-event bookings and finite prepared values. In the November 2026 review this check passed locally. Scikit-learn was unavailable in the review environment, so no complete model-training or interactive GUI run is claimed.

Random row splits can leak event-specific information; z-score-derived advertisement indicators do not demonstrate causal advertising effects. A future evaluation should hold out entire events and future dates and compare a naive booking baseline before using forecasts for decisions. Historical report scores are retained as submitted results, not fresh benchmark claims.

Academic work dates from 2024. The source maintenance, provenance documentation and redacted text derivatives are dated **14 November 2026**. Course briefs remain Keele material; team authorship is preserved. The presence of coursework does not grant a blanket licence over client data or other authors' work.
