# CNN-Parkinson-Disease

## Brief Description
Understanding of Parkinson's Disease through Explainable Artificial Intelligence (XAI) applied to speech measurements

## Dataset
* Tabular data. MS Excel file (csv format).
* 5875 rows of data (i.e., 5875 voice recordings).
* The dataset contains biomedical voice measurements from subjects with early-stage  Parkinson's  disease  recruited  to  a  six-month  trial of a telemonitoring device for remote symptom progression of Parkinson's disease  (Kancharla  Naveen  Kumar,  2023;  UCI  Machine  Learning Repository, no date).
* Source of the dataset:
  * Kaggle - Parkinson's Disease Detection Dataset:
    * https://www.kaggle.com/datasets/naveenkumar20bps1137/parkinsons-disease-detection/data?select=parkinsons.data
    * License: Creative Commons Attribution 4.0 International (CC BY 4.0).
  * UC Irvine Machine Learning Repository 
    * https://archive.ics.uci.edu/dataset/174/parkinsons
    * License: Creative Commons Attribution 4.0 International (CC BY 4.0).
* The dataset used in this project is not considered unbalanced because the 2:1 ratio displayed in this dataset (i.e., two males for every female) reflects  the  distribution  in  the  general  population  for  Parkinson’s disease.
* Columns of the dataset 
  * Independent features: 20 columns, where 17 correspond to biomedical voice measurement and 3 correspond to demographic information. They are the following: Subject, Age, Sex, test_time, Jitter (%), Jitter (Abs), Jitter: RAP, Jitter: PPQ5, Jitter: DDP, Shimmer, Shimmer(dB), Shimmer: APQ3, Shimmer: APQ5, Shimmer: APQ11, Shimmer: DDA, NHR, HNR, RPDE, DFA, and PPE
  * Dependent feature: 1 column (motor_UPDRS)

 ## Description
*  In  this  project,  the  machine  learning  model  of Boosted  Trees  was  applied  to  a  numeric  tabular  data  set,  and  the  deep  learning technique of convolutional neural networks was applied to images of 224x224 pixels, which were previously a numeric tabular dataset.
* In this project, the respective pipelines were developed and implemented to execute data processing, feature engineering, model application, model evaluation, and model comparison.
* SHAP (SHapley Additive exPlanations) was used for model interpretability.


![image](https://github.com/user-attachments/assets/fda3d91c-b523-447d-a353-ac19d0b6be60)

## Key Insights
* The Boosted Trees model achieved a Mean Absolute Error of 1.21 for the training phase and 1.23 for the testing phase on  the  metric  tabular  dataset;  meanwhile,  the  convolutional  neural  network achieved a Mean Absolute Error of 6.43 for the training phase and 6.52 for the testing phase on the image dataset. In addition, both models display 8 features in common 
in the top 10 features that have more impact on model prediction according to the Mean Shapley Value technique.
* The evidence suggests  that  changes  in  the  hyperparameters  and/or  architecture  of  the convolutional neural network are probably required, or the transformation of the numeric tabular data into images may not have been optimal, negatively impacting the convolutional neural network’s performance.
