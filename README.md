# Model Evaluation and Uncertainty Analysis of Common Swift (Apus apus) Migration Under Climate Change in Manchester :  Model Selection and Cross-Dataset Analysis
  EART60702_project2_group3

## 1\. Project Description

This project focuses on predicting the maximum urban temperatures in Greater Manchester to investigate the ecological impacts of climate change. By utilizing the **CESM (Community Earth System Model)** datasets, we evaluate and compare the performance of various Machine Learning (AutoML, XGBoost,Random Forest, LightGBM) and Deep Learning (MLP, LSTM, TFT) architectures.

A core objective is to understand how temperature variances influence the arrival dates of **Common Swifts** in the UK and their subsequent reproductive success, bridging the gap between climate modeling and conservation biology.

## 2\. Research Questions

1.  **Algorithm Optimization**: Can machine learning/deep learning significantly improve temperature prediction accuracy compared to traditional baseline models?
2.  **Sensitivity Analysis**: Do small initial differences in temperature data lead to divergent future temperature projections?
3.  **Ecological Impact**: How does rising temperature change the arrival dates of Common Swifts to the UK and impact their reproductive success?

## 3\. Data Sources

  * **Meteorological Data**:(https://www.cesm.ucar.edu/community-projects/lens/data-sets)
  * **Data Processing**: Original NetCDF (`.nc`) files have been pre-processed into CSV format for compatibility with the ML pipeline.
    
## 4\. Repository Structure

```text
├── AutoML/                # Automated ML experiments (003-008)
  ├──autoML_003.ipynb
  ├──autoML_004.ipynb
  ├──autoML_005.ipynb
  ├──autoML_006.ipynb
  ├──autoML_007.ipynb
  ├──autoML_008.ipynb
├── DeepLearning/          # DL Models with different splitting methods (MLP, LSTM, TFT for model election)
  ├──deep_learning_time_series_model_selection.ipynb
  ├──deep_learning_time_window_model_selection.ipynb
├── Preprocess/         # Preprocessing & Pre-processed Manchester climate CSV files
  ├──Data_manchester.zip
  ├──Kedi_Li_environment.yml
  ├──Processed_data_manchester.zip
  ├──Project_2_preprocess.ipynb
  ├──readme.txt
├── machine learning model selection/             # Experiment for machine learning model selection
  ├──005_split_model_compare.ipynb
  ├──005_windows_model_compare.ipynb
  ├──007_split_model_compare.ipynb
  ├──007_windows_model_compare.ipynb
├── prediction result      # Predict and result
  ├──dataset_03_predictions.csv
  ├──dataset_04_predictions.csv
  ├──dataset_06_predictions.csv
  ├──dataset_08_predictions.csv
  ├──predictions.csv
├── visualization          # Visualization of result, used in presentation
  ├──swift_arrical.ipynb
  ├──visualization.ipynb
├── All_datasets_EDA       # EDA for all datasets
├── Extended_visualization # Visualization
├── raw_data_distribution  # Data distribution for un-preprocessing data
└── README.md              # Main project documentation
```

## 5\. Model Performance

In terms of deep learning, MLP (Multi-Layer Perceptron) achieved the best performance. Within supervised learning, XGBoost performed optimally, yielding results close to AutoML; therefore, XGBoost was selected for the final dataset predictions.
| Model | MSE | RMSE | R-Square | Max Error |
| :--- | :---: | :---: | :---: | :---: |
| MLP | 0.563 | 0.739 | 0.979 | 4.863 |
| XGBoost (Best) | 0.517 | 0.688 | 0.983 | 4.689 |
| AutoML (Baseline) | 0.518 | 0.704 | 0.981 | 4.254 |

## 6\. Conclusions
  * **Optimal Algorithm**: XGBoost is the best-performing model, with results most closely aligned with the baseline, demonstrating its robustness in temperature forecasting.

  * **Initial Conditions Cause Difference**: Small initial atmospheric factors introduced into the models lead to significantly different predicted temperatures, highlighting the chaotic nature of climatic variables.

  * **Ecological Response**: Common Swift migration timing is highly sensitive to temperature fluctuations. Higher temperatures and earlier arrivals have been found to improve laying and overall reproductive success.

## 7\. Contributors

  * **Group 3** - EART60702 Project 2
  * Members: Emmaunel Julius, Kedi Li, Jing Chen, Yuqing Liu

-----
