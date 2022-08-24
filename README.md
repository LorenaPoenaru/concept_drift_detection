# Are Concept Drift Detectors Reliable Alarming Systems? - A Comparative Study
## Data 
Explanations about where to download the real-world data and how to generate the synthetic data can be found in _data_.
## Experimental Code
#### Synthetic Data Code
The code for synthetic data for both error based detectors and data distribution based detectors can be found in _synthetic_data_code_. This scripts cover all the cases analyzed: all random seeds, all datasets, all noise values, all drift types and both balanced and imbalanced classes.
#### Real-world Data Code
The code for real-world data for both datasets, Energy (ELECT2) and Airlines, can be found in _real_world_data_code_. Both types of drift detectors are evaluated within one script corresponding to the dataset.
## Implementation of data distribution based drift detectors.
We openly share the implementation of 3 data distribution based drift detectors: EDE, kdqTrees and PCA-kdq. Details about implementation decisions can be found in the paper. These function can be used for any other dataset besides the ones employed by us.
#### EDE
Implementation can be found in every script as function _ede_drift_detector_. The function requires the distribution of the reference data and the distribution of the testing data as parameters.
#### kdqTrees & PCA-kdq
Implementation can be found in every script as function _kdqtrees_bootstrapping_. The function requires 4 parameters, namely the _distribution of the reference data_, the _distribution of the testing data_, the _**output for the bootstrapping function**_ and the _**distance**_. The output of the bootstrapping function can be obtained running the function _bootstrapping_. This function requires as parameters the _reference data_, the _number of reference data subsamples used for the bootstrapping technique_ and the _pca_ parameter, which indicates whether PCA is applied on the data. The pca parameter should be None for kdqTrees only. The _distance_ takes the following values ['kl_divergence', 'manhattan', 'chebyshev', 'kulsinski', 'cosine', 'squared_euclidean', 'bhattacharyya'].
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


