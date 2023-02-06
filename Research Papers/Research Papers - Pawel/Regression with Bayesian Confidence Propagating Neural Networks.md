Link: [[Thesis - Raghav Bongole - Regression_with_Bayesian_Confidence_Propagating_Neural_Networks.pdf]]

----

**Aim and scope**
This project aims to investigate whether [[BCPNN (Bayesian confidence propagation neural network)]] can be extended to predict continuous-valued data, whereas it now mainly predicts discrete variables. The model will be compared with a simple Ridge Regressor baseline.

**Method**
To predict continuous-valued data, the paper encodes the data into discrete variables using Gaussian Mixture Models (GMMs) and Interval Encoding. So in a sense, the problem is reduced back to the typical problems.

**Results**
The method is then evaluated on the Parkinson dataset, and some Protein-folding dataset. It seems to achieve good results. However, the training seemed to take very long time.