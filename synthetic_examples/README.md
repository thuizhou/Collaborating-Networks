### Evaluate the performance of CN in synthetic examples.
We include two synthetic examples in two folders syn-1, syn-2.
Within each folder, the name of each notebook indicates the cooresponding method.

* CN_TH.ipynb: CN and the ground truth 
* DP.ipynb: MC dropout
* CQR.ipynb: conformalized quantile regression
* g-only.ipynb: learning cdf with g in CN, and fix f as uniform distribution
* EN.ipynb: deep ensemble model 




#### syn-1: Heteroskedastic Gaussian Example
The synthetic data follows a Gaussian distribution with a unique mean and variance value for each sample. The synthetic procedure is included in each notebook within the folder. We generate 700 training samples and 300 evaluation samples. 

CN more faithfully generate the true 90% intervals for each sample:

[CQR](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/cqrwidth.pdf)|
[EN and DP](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/endpwidth.pdf)|
[g-only](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/gwidth.pdf)|
[CN](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/gfwidth.pdf)


CN recover the ground truth CDF:
[Gaussian Example 1](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/syn1dist1.pdf)|
[Gaussian Example 2](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/syn2dist2.pdf)


#### syn-2: Weibull Distribution Example
The synthetic data follows a Weibull distribution with a unique scale and shape parameter for each sample. The synthetic procedure is included in each notebook within the folder. We generate 700 training samples and 300 evaluation samples. 


CN more faithfully estimate the survival probability P(Y_i>1|X_i)
[CN with f](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/cnfsuv1.pdf)|
[CN with g](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/cngsuv1.pdf)|
[EN and DP](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/endpsuv1.pdf)|
[g-only](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/gsuv1.pdf)


CN recover the ground truth survival function(1-CDF).
[Weibull Example 1](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/syn2suv1.pdf)|
[Weibull Example 2](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-2/syn2suv2.pdf)



