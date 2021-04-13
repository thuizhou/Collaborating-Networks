### Evaluate the performance of CN in Real Data.
We include five six data examples in the article. Four are form UCI datasets: http://archive.ics.uci.edu/ml/datasets. One is from Kaggle datasets:  https://www.kaggle.com/. The last dataset considered is an electronic health records developed from the Southeastern Diabetes Initiative (SEDI), whose analysis was executed within the Duke Protected Analytics Computing Environment (PACE), so we do not include this example here.


We demonstrate the implementation of each method in the [Energy dataset](https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Energy/). For other datasets, we only include their preprocessing steps, and their experiments are conducted with identical steps. 

We included the following methods for each datasets.

* CN.ipynb: CN.
* g-only.ipynb: learning cdf with g in CN, and fix f as uniform distribution
* DP_CR.ipynb: MC dropout with and without recalibration.
* CDP.ipynb: concrete dropout.
* CQR.ipynb: conformalized quantile regression.
* EN.ipynb: deep ensemble model. 
* GPR.ipynb: exact gaussain process regressor.
* PPGPR.ipynb: paramatric gaussain process regressor.
* g-only.ipynb: learning cdf with g in CN, and fix f as uniform distribution

 
 
#### CPU
The CPU dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/Computer+Hardware

Calibration and sharpness:
<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/CPU/cpuc.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/CPU/cpul.png">
</p>



#### Energy
The Energy dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/Individual+household+electric+power+consumption

Calibration and sharpness:
<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Energy/energyc.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Energy/energyl.png">
</p>



#### MPG
The MPG dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/auto+mpg

Calibration and sharpness:
<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/MPG/mpgc.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/MPG/mpgl.png">
</p>



#### Crime
The Crime dataset is downloaded from http://archive.ics.uci.edu/ml/datasets/communities+and+crime

Calibration and sharpness:
<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Crime/crimec.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Crime/crimel.png">
</p>



### Airline  
The Airline dataset is downloaded from https://www.kaggle.com/giovamata/airlinedelaycauses. 

Calibration and sharpness:
<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Airline/airc.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Airline/airl.png">
</p>




