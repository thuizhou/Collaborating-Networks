### Evaluate the performance of CN in synthetic examples.
We include two synthetic examples in two folders syn-1, syn-2.
Within each folder, the name of each notebook indicates the cooresponding method.

* CN_TH.ipynb: CN-g CN-f and the ground truth 
* g-only.ipynb: learning cdf with g in CN, and fix f as uniform distribution
* DP.ipynb: MC dropout
* CDP.ipynb: concrete dropout
* CQR.ipynb: conformalized quantile regression
* EN.ipynb: deep ensemble model 
* GPR.ipynb: exact gaussain process regressor
* PPGPR.ipynb: paramatric gaussain process regressor





#### syn-1: Heteroskedastic Gaussian Example
The synthetic data follows a Gaussian distribution with a unique mean and variance value for each sample. The synthetic procedure is included in each notebook within the folder.

CN more faithfully generate the true 90% intervals for each sample:


<p align="center">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/gfwidth.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/gowidth.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/enwidth.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/dpwidth.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/gpwidth.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/cqrwidth.png">
</p>




CN recover the ground truth CDF (2 random samples):
<p align="center">
  <img width="460" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/syn1TH1.png">
  <img width="460" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/syn1TH2.png">
</p>



#### syn-2: Weibull Distribution Example
The synthetic data follows a Weibull distribution with a unique scale and shape parameter for each sample. The synthetic procedure is included in each notebook within the folder. 


CN more faithfully estimate the survival probability P(Y_i>1|X_i)
<p align="center">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/cngsuv1.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/cnfsuv1.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/gosuv1.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/ensuv1.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/dpsuv1.png">
  <img width="320" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/gpsuv1.png">
</p>



CN recover the ground truth weibull function(2 random samples).

CN more faithfully estimate the survival probability P(Y_i>1|X_i)
<p align="center">
  <img width="460" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/syn2TH1.png">
  <img width="460" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/syn2TH2.png">
</p>




