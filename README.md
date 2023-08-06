# Early-Prediction-for-Sepsis
## Background
### Introduction
In this data challenge, we will use information collected during the stay of a patient in ICU to predict whether the patient will develop sepsis (0 for no sepsis and 1 for sepsis).  The data consist of records from 21634 patients and has been split into a training set (with 15144 patients) and a test set (with 6490 patients).  Outcomes are provided for the training set, and are withheld for the test set.

### Prediction Variables

Approximately 40 variables were recorded at least once after the patient's admission to the ICU.  Several of these variables are general descriptors (such as age, gender, and the ICU unit), and the remainder are clinical vital signs and laboratory measurements, for which multiple observations may be available.  Each vital sign or laboratory measurement has an associated time-stamp indicating the elapsed time (in hours) of the measurement since ICU admission.  Thus, for example, a time stamp of 3 means that the associated measurement was made 3 hours after the patient was admitted to the ICU.

Each patient's record is stored as a comma-separated value (CSV) text file, and descriptions of the prediction variables are given below.

### Vital signs

- HR: Heart rate (beats per minute)
- O2Sat: Pulse oximetry (%)
- Temp: Temperature (Deg C)
- SBP: Systolic BP (mm Hg)
- MAP: Mean arterial pressure (mm Hg)
- DBP: Diastolic BP (mm Hg)
- Resp: Respiration rate (breaths per minute)
- EtCO2: End tidal carbon dioxide (mm Hg)
- Laboratory values

- BaseExcess: Measure of excess bicarbonate (mmol/L)
- HCO3: Bicarbonate (mmol/L)
- FiO2: Fraction of inspired oxygen (%)
- pH: N/A
- PaCO2: Partial pressure of carbon dioxide from arterial blood (mm Hg)
- SaO2: Oxygen saturation from arterial blood (%)
- AST: Aspartate transaminase (IU/L)
- BUN: Blood urea nitrogen (mg/dL)
- Alkalinephos: Alkaline phosphatase (IU/L)
- Calcium: (mg/dL)
- Chloride: (mmol/L)
- Creatinine: (mg/dL)
- Bilirubin_direct: Bilirubin direct (mg/dL)
- Glucose: Serum glucose (mg/dL)
- Lactate: Lactic acid (mg/dL)
- Magnesium: (mmol/dL)
- Phosphate: (mg/dL)
- Potassium: (mmol/L)
- Bilirubin_total: Total bilirubin (mg/dL)
- TroponinI: Troponin I (ng/mL)
- Hct: Hematocrit (%)
- Hgb: Hemoglobin (g/dL)
- PTT: partial thromboplastin time (seconds)
- WBC: Leukocyte count (count*10^3/µL)
- Fibrinogen: (mg/dL)
- Platelets: (count*10^3/µL)
- Demographics

- Age: Years (100 for patients 90 or above)
- Gender: Female (0) or Male (1)
- Unit1: Administrative identifier for ICU unit (MICU)
- Unit2: Administrative identifier for ICU unit (SICU)

### Evaluation Metrics

The prediction results will be rated with the balanced error rate (BER = the average of the error rate on positive class examples and the error rate on negative class examples) and the area under the receiver operating characteristic curve (AUC).

### Remark

This data challenge was adapted from the following website:

https://physionet.org/content/challenge-2019/1.0.0/

## Results
- test_withlabel.csv
- model_structure.pdf
- 3. all other source files

## Programs:
- 1_preprocess.ipynb: This program will generate the intermediate files
    "x_train.csv" and "x_test.csv".
- 2_EDA.ipynb: EDA program and some insights
- 3_model.ipynb: This is the main part of the model. It contains training,
    validation, and prediction using 10-fold cross-validation.

## Data:
- train_outcome.csv: raw data
- test_nolabel: empty csv
- x_train: intermediate data files
- x_test: intermediate data files
