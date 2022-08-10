# Synthetic Data Generation using MOA Framework

## MOA 

The MOA Framework can be found at the following link: https://moa.cms.waikato.ac.nz and it can be downloaded and installed according to the instructions on this website.

## Version

For this project we used MOA Release 2020.12.0.

## Commands for Data Generation

MOA Datasets can be generated through specific commands. Explanation about MOA commands can be found in the MOA Manual: https://moa.cms.waikato.ac.nz/wp-content/uploads/2010/05/Manual.pdf

Comment: In all cases the number following the -i shows the random seed used. Here we give examples with random seed 1, but any random seed can be selected. All these commands will generate .arff files containing the streaming data.

### SEA Dataset

#### Abrupt Drift

##### Ideal Conditions:

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.SEAGenerator -f 3 -b -n 0 -i 1) -d (generators.SEAGenerator -f 2 -b -n 0 -i 1) -p 55000 -w 1) -f sea_1_abrupt_drift_0_noise_balanced.arff -m 100000_

##### Non-Ideal Conditions:

**Noise 10%:**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.SEAGenerator -f 3 -b -n 0 -i 1) -d (generators.SEAGenerator -f 2 -b -n 10 -i 1) -p 55000 -w 1) -f sea_1_abrupt_drift_10_noise_balanced.arff -m 100000_

**Noise 20%:**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.SEAGenerator -f 3 -b -n 0 -i 1) -d (generators.SEAGenerator -f 2 -b -n 20 -i 1) -p 55000 -w 1) -f sea_1_abrupt_drift_20_noise_balanced.arff -m 100000_

**Class Imbalance**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.SEAGenerator -f 3 -n 0 -i 1) -d (generators.SEAGenerator -f 2 -n 0 -i 1) -p 55000 -w 1) -f sea_1_abrupt_drift_0_noise_imbalanced.arff -m 100000_

#### Gradual Drift

### AGRAW1 Dataset

#### Abrupt Drift

##### Ideal Conditions:

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.AgrawalGenerator -f 1 -b -p 0 -i 1) -d (generators.AgrawalGenerator -f 6 -b -p 0 -i 1) -p 55000 -w 1) -f agraw1_1_abrupt_drift_0_noise_balanced.arff -m 100000_

##### Non-Ideal Conditions:

**Noise 10%**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.AgrawalGenerator -f 1 -b -p 0 -i 1) -d (generators.AgrawalGenerator -f 6 -b -p 0.1 -i 1) -p 55000 -w 1) -f agraw1_1_abrupt_drift_10_noise_balanced.arff -m 100000_

**Noise 20%**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.AgrawalGenerator -f 1 -b -p 0 -i 1) -d (generators.AgrawalGenerator -f 6 -b -p 0.2 -i 1) -p 55000 -w 1) -f agraw1_1_abrupt_drift_20_noise_balanced.arff -m 100000_

**Class Imbalance**

_WriteStreamToARFFFile -s (ConceptDriftStream -s (generators.AgrawalGenerator -f 1 -p 0 -i 1) -d (generators.AgrawalGenerator -f 6 -p 0 -i 1) -p 55000 -w 1) -f agraw1_1_abrupt_drift_0_noise_imbalanced.arff -m 100000_

### AGRAW2
