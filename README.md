# Are Concept Drift Detectors Reliable Alarming Systems? - A Comparative Study
## Data 
Explanations about where to download the real-world data and how to generate the synthetic data can be found in _data_.
## Experimental Code
#### Synthetic Data Code
The code for synthetic data for both error based detectors and data distribution based detectors can be found in _synthetic_data_code_. This scripts cover all the cases analyzed: all random seeds, all datasets, all noise values, all drift types and both balanced and imbalanced classes.
#### Real-world Data Code
The code for real-world data for both datasets, Energy (ELECT2) and Airlines, can be found in _real_world_data_code_. Both types of drift detectors are evaluated within one script corresponding to the dataset.
## Versions
python=3.8.8 

imbalanced-learn=0.9.0

jupyter=1.0.0

lightgbm=3.2.1

numpy=1.20.2

pandas=1.2.4

scikit-learn=1.0.2

scikit-multiflow=0.5.3

scipy=1.6.3

seaborn=0.11.1

statsmodels=0.13.2

xgboost=1.4.2


