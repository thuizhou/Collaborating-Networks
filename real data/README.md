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
The preprocess is performed [cpu preprocess](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/CPU/cpu_preprocess.ipynb), with the resulted training and testing data: train.npy,test.npy



The overall model calibration: [calcpu](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/CPU/cpuc.pdf)

The overall model sharpness: [shpcpu](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/CPU/cpul.pdf)



#### Energy
The Energy dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/Individual+household+electric+power+consumption
The preprocess is performed in [energy preprocess](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Energy/energy_preprocess.ipynb), with the resulted training and testing data: train.npy,test.npy




The overall model calibration: [calen](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Energy/energyc.pdf)

The overall model sharpness: [shpen](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Energy/energyl.pdf)




#### MPG
The MPG dataset is downloaded from https://archive.ics.uci.edu/ml/datasets/auto+mpg
The preprocess is performed in [mpg preprocess](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/MPG/mpg_preprocess.ipynb), with the resulted training and testing data: train.npy,test.npy




The overall model calibration: [calmpg](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/MPG/mpgc.pdf)

The overall model sharpness: [shpmpg](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/MPG/mpgl.pdf)






#### Crime
The Crime dataset is downloaded from http://archive.ics.uci.edu/ml/datasets/communities+and+crime
The preprocess is performed in [crime preprocess](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Crime/crime_preprocess.ipynb), with the resulted training and testing data: train.npy,test.npy



The overall model calibration: [calcri](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Crime/crimec.pdf)

The overall model sharpness: [shpcri](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/Crime/crimel.pdf)




