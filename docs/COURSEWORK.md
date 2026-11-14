# Coursework and contribution evidence

## Assessment context

This is a 2023/24 MSc Computer Science module project, worth 15 CATS, with an overall module mark of 77%. The verified private transcript establishes that result. The public [2023/24 module specification](https://www.keele.ac.uk/catalogue/2023-24/csc-40038.htm) places the work in small-team development for a real client: 50% group presentation and application documentation, 25% weekly team diaries and 25% individual reflection. Those weightings explain the collaborative context; they are not separate marks awarded to this repository.

## Source walkthrough

| Skill | Repository evidence | Interpretation |
| --- | --- | --- |
| Data preparation | `Prediction Model and GUI/DataPrep.py` | Seven named event files are paired with explicit event dates, filled onto daily timelines and grouped by target audience. |
| Exploratory analysis | `Data Analysis/dataAnalysis.py`, `original-work/Data-Analytics/FinalAnalytics.py` | Weekly bookings are summarised using mean, standard deviation and z-scores, with plots and spreadsheet exports. |
| Forecasting | `Prediction Model and GUI/FinalModel.py` | ElasticNet cross-validation uses day number and an inferred advertisement flag to predict bookings. |
| Attendance classification | `Prediction Model and GUI/FutureWorkPrediction.py` | Logistic regression explores attendance from the imputed event files. |
| Alternative approaches | `Regression Models/`, `Classification Models/`, `Time Series Models/` | Historical model exploration is available for inspection without presenting all scripts as one clean production pipeline. |
| Missing data | `Data Imputation/` | Experiments compare ways to fill incomplete booking information. |
| Interface integration | `Prediction Model and GUI/GUI.py` | Tkinter collects date, booking and audience inputs and presents prediction results. |
| Collaborative development | Student-report extracts | Team roles and the change from a web prototype to a GUI are documented. |

## My contribution and team boundaries

My personal reflection describes developing ten successive Python data-analysis programs, checking results against a teammate's Excel work and building a React frontend with a Flask backend prototype. It also explains why the team chose a GUI when the final model integration arrived close to submission. This is historical self-report evidence. The React/Flask prototype source was not found in this repository, so there is no launch or deployment claim for that prototype.

The reflection assigns data analysis to me and one teammate, missing-data research to other teammates, and prediction-model research and preparation to a separate subgroup. The [group technical report extract](original/group-coursework-technical-text.md) documents the combined solution. The project is credited as group work rather than my sole implementation. Colleague identifiers and private peer assessments are excluded from the public extracts.

## Data and scientific interpretation

The seven raw CSV files are `D19`, `D21`, `GP21`, `MSE21`, `NP21`, `SRM22` and `SRM23`, alongside corresponding imputed versions. Their second row is the header. The fields include booking reference, creation date, reference, attendee status and attended status. The preparation code primarily aggregates counts by day and week. Booking references are historical source fields, not user accounts or authentication credentials.

The model assumes useful transfer between events in the same audience category. It infers advertising periods from unusual booking activity rather than an independently observed intervention. Outlier removal and imputation can change results. Random train/test splits within these small event collections should not be interpreted as a prospective test on a new conference.

## Original work and 2026 maintenance

The root source and `original-work/` record coursework and later maintenance. The preserved import has its own byte-level provenance and is not rewritten by this documentation review. The 2026 synthetic browser illustration is separate from the assessed software.

The November 2026 update adds navigable evidence, distinguishes individual contribution from the team product, records source hashes and makes the maintained attendance-data paths portable. It does not revise the submitted report, award a new mark or claim a new trained model. The source DOCX files remain privately retained; the extracts explicitly state their omissions.
