# Flight Trajectory Prediction with the System-Wide Information Management (SWIM) Data

In this project, we build two Bayesian neural networks to predict the trajectory of an ongoing flight. The first model is built with a feedforward neural network with the goal to predict the trajectory deviation from the filed flight plan, while the second model is built with the Long-Short Term Memory (LSTM) neural network to make longer-term prediction on the flight trajectory. The two models are combined together to achieve high prediction accuracy and longer-term prediction capability. The uncertainty in both models is characterized following a Bayesian approach and implemented through Monte Carlo (MC) dropout. 

## Getting Started

* This repository is used to show the detailed procedures in the development of Bayesian deep learning models, where flight AA598 is used as an illustrative example. 
* We proprecess the trajectory data of flight AA598 to remove anomalous positions, and impute the missing data with linear interpolation. The trajectory of the flight AA598 from 19th December, 2018 to 8th February, 2019 is saved as a pickle file named as "AAL598_2018-12-19-2019-02-08.pkl" in the repository (Note: the trajectory over some days are missing).
* Leave-one-out cross-validation is performed to check the performance of the trained models.

### Prerequisites

The following packages need to be installed to run this program

```
tensorflow
keras
sklearn
pytorch 
matplotlib
numpy
math
copy
pandas
pickle
```

## Acknowledgments

* The research reported in this paper was supported by funds from NASA University Leadership Initiative program (Grant No. NNX17AJ86A, Technical Monitor: Dr. Kai Goebel) through subcontract to Arizona State University (Principal Investigator: Dr. Yongming Liu). 
* The support of FAA and Harris Corporation in accessing the SWIM data is appreciated. 
* This work was conducted in part using the resources of the Advanced Computing Center for Research and Education (ACCRE) at Vanderbilt University, Nashville, TN, USA.
