# ML Monitoring - Feature importance weighted drift detection and automated-retraining

## Overview

Every model over time is impacted by model performance decay due to data drift and concept drift. One of many solution is to perform drift detection and set up automated retraining of the model. Drift in every feature does't have the same impact on model performance. In this project we combine feature importance of a particular feature with its drift score obtained through statistical test to determine wether to retrain model or not. Thus model will be retrained only when there is drift on features with higher importance and also when feature with lower importance faces higher data drift.

## Dataset:

* Contains warehouse demand data from 2017-01-01 to 2020-11-15
* Working with preprocessed data
* No data leakage as missing values were filled without requirement of any transformation

## Assumptions

* Initial model deployment on march 2019
* True labels/ actual demand available over the weekend
* Model monitored on weekly basis




