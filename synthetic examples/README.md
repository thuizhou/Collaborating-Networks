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
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)

CN recover the ground truth CDF.

#### syn-2: Weibull Distribution Example
The synthetic data follows a Weibull distribution with a unique scale and shape parameter for each sample. The synthetic procedure is included in each notebook within the folder. We generate 700 training samples and 300 evaluation samples. 


CN more faithfully estimate the survival probability P(Y_i>1|X_i)
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)
![calib](Het_Gaussian_CN/calibration.png)

CN recover the ground truth survival function(1-CDF).




