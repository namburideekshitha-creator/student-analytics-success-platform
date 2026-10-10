# CampusPulse — Student Success Analytics

A standalone, responsive dashboard prototype for the Smart Campus Analytics challenge. No server, framework, or build step is required.

## Run it

Open `index.html` in a recent browser. The prototype includes a 54-student illustrative cohort, dashboard metrics, score distribution, performance drivers, interactive segments, searchable/filterable student directory, student score explanations, an intervention planning form, and CSV export.

## Student Success Score

Score = 35% academic progress + 20% attendance + 15% LMS engagement + 20% placement readiness + 10% engagement/feedback. Academic progress is normalized CGPA (CGPA × 10), reduced by 5 points per backlog and bounded at 0–100. Engagement/feedback is the mean of event/club/certification engagement and satisfaction feedback. The score is rounded to an integer.

Risk rules: High if score <55, attendance <65%, or backlogs ≥2; Medium if score <70, placement readiness <55%, or LMS engagement <55%; otherwise Low. These are transparent demonstration thresholds, not a validated predictive model. Calibrate using institutional outcomes and keep human review in any real deployment.

## Data and production notes

`app.js` starts from one normalized illustrative array with academic, attendance, LMS, engagement, placement, feedback and skills assessment values. Replace it with consented, access-controlled integrations and document data freshness, missingness, role permissions, retention and bias review. The intervention form demonstrates workflow only; it does not persist or contact students.
