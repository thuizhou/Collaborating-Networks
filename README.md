# Collaborating-Networks

This repository contains the code associated with examples of paper by Zhou, Li, Yuan and Carlson. The manuscript is now available on Arxiv (https://arxiv.org/abs/2002.05212). These examples illustrate how to use collaborating networks(CN) to estimate the conditional distribution Y|X=x of continuous outcome.
Specifically, one network (g) approximates the cumulative distribution function, and the second network (f) approximates its inverse.





## Methods for Comparison
We include four other methods also capable of estimating full distribution. They are:

* Conformalized Quantile Regression(CQR):https://github.com/yromano/cqr

[1] Yaniv Romano, Evan Patterson, and Emmanuel J. Candes. [“Conformalized quantile regression.”](https://arxiv.org/abs/1905.03222) 2019. 

* MC dropout(DP):https://github.com/yaringal/DropoutUncertaintyExps/blob/master/net/net.py

[2]Gal, Yarin, and Zoubin Ghahramani. ["Dropout as a bayesian approximation: Representing model uncertainty in deep learning." international conference on machine learning".](http://proceedings.mlr.press/v48/gal16.pdf) 2016

* Deep Ensembles(EN)

[3]Lakshminarayanan, Balaji, Alexander Pritzel, and Charles Blundell. ["Simple and scalable predictive uncertainty estimation using deep ensembles."](http://papers.nips.cc/paper/7219-simple-and-scalable-predictive-uncertainty-estimation-using-deep-ensembles.pdf) 2017.

* Calibrated Regression(CR)

[4] Kuleshov, Volodymyr, Nathan Fenner, and Stefano Ermon, ["Accurate uncertainties for deep learning using calibrated regression."](https://arxiv.org/pdf/1807.00263.pdf) 2018.




## Experimental Details

1. [property of learning f](https://github.com/thuizhou/Collaborating-Networks/tree/main/property%20of%20learning%20f): CN's stability under overparameterization, and the merit of learning g and f jointly over learning g alone with a fixed f. 
2. [synthetic examples](https://github.com/thuizhou/Collaborating-Networks/tree/main/synthetic%20examples): Two synthetic examples simulated from Gaussian and Weibull Distribution
3. [real data](https://github.com/thuizhou/Collaborating-Networks/tree/main/real%20data): Four real data examples with data available at: http://archive.ics.uci.edu/ml/datasets.


Overall:

* CN has great recovery of the ground truth distribution in the synthetic examples:

[Gaussian Sample](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic%20examples/syn-1/syn1dist1.pdf)


* CN has faithfull interval coverage(calibration)

[Calibration plot](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/CPU/cpuc.pdf)

* CN increases the interval sharpness:

[Sharpness plot](https://github.com/thuizhou/Collaborating-Networks/blob/main/real%20data/CPU/cpul.pdf)






## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
