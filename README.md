# Evaluate ML models at different hospitals

Code to complement the evaluation presented in "An evaluation of ML based clinical risk prediction applications in different hospitals". 

### 1. Data sharing

The patient data used in this evaluation from the three hospitals cannot be made publicly available due to patient protection.

### 2. Code organization

#### 2.1 Data preprocessing
The notebook `1-preprocessing.ipynb` is used to pre-process the log data. It aggregates the logs from the whole period to be studied, extracts the predictions, and transforms them into a dataframe to be easily used. 

#### 2.2 Characteristic of logging dataset.
The notebook `2-Log_data_characteristic_analysis` shows the characteristics of the features groups contained in the log files. So, it represents the characteristics of the data from the live clinical workflow.

#### 2.3 Model performance evaluation 
This part contains two notebooks `3-Model_performance_in_live_clinical_setting_with_log_data` and `4-Cross_hospital_model_performance_evaluation`. The first notebook evaluates the model performance trained in a specific hospital (e.g. Hospital H), in live data from the same hospital (e.g. Hospital H). The second one also evaluates the performance of two models that are trained in several hospitals (e.g. Hospital M and hospital N), in the live data from a different hospital (e.g. Hospital H). This allows us to simulate the performance of these models as if they are installed in the live clinical workflow at a certain hospital. 

#### 2.4 Model performance simulation 
This section also contains two notebooks `5-Simulate_model_performance_in_the_live_clinical_workflow` and `6-Simulate_model_performance_in_the_live_clinical_workflow-cross_hospital_evaluation`. As before, those notebooks simulates the risk prediction during a medical stay in the live EHR system in two different situations (model trained and evaluated in the same hospital or in a different one). 

#### 2.4 Model performance comparison
The notebook `7-Visualization` shows the differences between the live and the retrospective evaluation as well as the performance degradation in cross-hospital evaluation.
