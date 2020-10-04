### Evaluate the performance of CN in Real Data.
We include five real data examples in the article. Four are form UCI dataset. http://archive.ics.uci.edu/ml/datasets. The last dataset considered is an electronic health records developed from the Southeastern Diabetes Initiative (SEDI), whose analysis was executed within the Duke Protected Analytics Computing Environment (PACE), so we do not include this example here.

Within each folder, the name of each notebook indicates the cooresponding method.

* CN.ipynb: CN.
* DP_CR.ipynb: MC dropout with and without recalibration.
* CQR.ipynb: conformalized quantile regression.
* g-only.ipynb: learning cdf with g in CN, and fix f as uniform distribution.
* EN.ipynb: deep ensemble model 




#### CPU
The CPU dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/Computer+Hardware
The preprocess is performed in cpu_preprocess.ipynb, with the resulted training and testing data: train.npy,test.npy



The overall model calibration:
![calcpu](Het_Gaussian_CN/calibration.png)

The overall model sharpness:

![shpcpu](Het_Gaussian_CN/calibration.png)



#### Energy
The Energy dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/Individual+household+electric+power+consumption
The preprocess is performed in cpu_preprocess.ipynb, with the resulted training and testing data: train.npy,test.npy




The overall model calibration:
![calen](Het_Gaussian_CN/calibration.png)

The overall model sharpness:

![shpen](Het_Gaussian_CN/calibration.png)




#### MPG
The MPG dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/auto+mpg
The preprocess is performed in cpu_preprocess.ipynb, with the resulted training and testing data: train.npy,test.npy




The overall model calibration:
![calmpg](Het_Gaussian_CN/calibration.png)

The overall model sharpness:
![shpmpg](Het_Gaussian_CN/calibration.png)






#### Crime
The Crime dataset is downloaded from http://archive.ics.uci.edu/ml/datasets/communities+and+crime
The preprocess is performed in cpu_preprocess.ipynb, with the resulted training and testing data: train.npy,test.npy



The overall model calibration:
![calcri](Het_Gaussian_CN/calibration.png)

The overall model sharpness:

![shpcri](Het_Gaussian_CN/calibration.png)




