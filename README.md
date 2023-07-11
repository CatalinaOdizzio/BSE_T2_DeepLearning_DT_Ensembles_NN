# Length of stay prediction

Coursework for the course Deep Learning, taught in Term 2, at the Barcelona School of Economics. Kaggle competition: https://www.kaggle.com/competitions/dl23-length-of-stay-prediction-decision-trees

## Homework instructions:

In this project, you have to predict the length of stay (in days) of a patient that is entering an ICU (Intensive Care Unit) using decision tree models, ensembles and neural networks.

The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv corresponds to one ICU stay (hadm_id+ icustay_id) of one patient (subject_id). Column HOSPITAL_EXPIRE_FLAG is the indicator of death (=1) as a result of the current hospital stay; this is the outcome to predict in our modelling exercise. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv.

Please don't use any feature that you infer you don't know the first day of a patient in an ICU, e.g. HOSPITAL_EXPIRE_FLAG

Note that the main cause/disease of patient condition is embedded as a code at ICD9_diagnosis column. The meaning of this code can be found at MIMIC_metadata_diagnose.csv. But this is only the main one; a patient can have co-occurrent diseases (comorbidities). These secondary codes can be found at extra__data/MIMIC_diagnoses.csv.

As performance metric, please use RMSE (root mean squared error).
