# ML Monitoring - Feature importance weighted drift detection and automated-retraining

## Overview

Every model over time is impacted by model performance decay due to data drift and concept drift. One of many solution is to perform drift detection and set up automated retraining of the model. Drift in every feature does't have the same impact on model performance. In this project we combine feature importance of a particular feature with its drift score obtained through statistical test to determine wether to retrain model or not. Thus model will be retrained only when there is drift on features with higher importance and also when feature with lower importance faces higher data drift.

## Dataset:

* Contains warehouse demand data from 2017-01-01 to 2020-11-15

## Assumptions

* Initial model deployment on march 2019
* True labels/ actual demand available over the weekend
* Model monitored on weekly basis

## How feature importance weighted data drift is calculated?


### get drift scores provided train and production data


##### drift detected without feature importance wightage for these features - statewise_population_per_sqmile.value, warehouse_ID.value, Product_Type.value, state.value, county.value	

### Obtain feature importance

### Convert raw feature importance to relative feature importance based on the most important feature for the model

### Calculate feature importance weighted drift score by combining relative feature importance with drift score. Based on p-value obtain updated drift detected columns



##### drift detected with feature importance wightage for these features - statewise_population_per_sqmile.value, warehouse_ID.value, Product_Type.value	
<b>state.value and county.value are not detected because of high feature importance weighted p_value</b>
