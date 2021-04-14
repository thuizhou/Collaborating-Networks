# Collaborating-Networks

This repository contains the code associated with examples of paper by Zhou, Li, Yuan and Carlson. The manuscript is now available on Arxiv (https://arxiv.org/abs/2002.05212). These examples illustrate how to use collaborating networks(CN) to estimate the conditional distribution Y|X=x of continuous outcome.
Specifically, one network (g) approximates the cumulative distribution function, and the second network (f) approximates its inverse.




## Methods for Comparison
We include four other methods also capable of estimating full distribution. They are:


* MC dropout(DP):https://github.com/yaringal/DropoutUncertaintyExps/blob/master/net/net.py [1]

* Calibrated Regression(CR) [2]

* Concrete dropout(CDP):https://github.com/yaringal/ConcreteDropout [3]

* Gaussian Process Regressor(GPR):https://docs.gpytorch.ai/en/v1.1.1/examples/01_Exact_GPs/ 

* Parametric Gaussian Process Regressor (PPGRP): https://docs.gpytorch.ai/en/v1.1.1/marginal_log_likelihoods [4]

* Conformalized Quantile Regression(CQR):https://github.com/yromano/cqr [5]

* Deep Ensembles(EN): https://blog.tensorflow.org/2019/03/regression-with-probabilistic-layers-in.html [6]




[1] Gal, Yarin, and Zoubin Ghahramani. ["Dropout as a bayesian approximation: Representing model uncertainty in deep learning." In International Conference on Machine Learning,] (http://proceedings.mlr.press/v48/gal16.pdf) 2016.

[2] Kuleshov, Volodymyr, Nathan Fenner, and Stefano Ermon, ["Accurate uncertainties for deep learning using calibrated regression." In International Conference on Machine Learning,] (http://proceedings.mlr.press/v80/kuleshov18a/kuleshov18a.pdf) 2018.

[3] Gal, Y., Hron, J. and Kendall, ["Concrete dropout." In International Conference on Neural Information Processing Systems,] 
(https://proceedings.neurips.cc/paper/2017/file/84ddfb34126fc3a48ee38d7044e87276-Paper.pdf) 2017.

[4] Jankowiak, Martin, Geoff Pleiss, and Jacob Gardner, ["Parametric Gaussian process regressors." In International Conference on Machine Learning,] (http://proceedings.mlr.press/v119/jankowiak20a/jankowiak20a.pdf) 2020.


[5] Yaniv Romano, Evan Patterson, and Emmanuel J. Candes. [“Conformalized quantile regression.” In International Conference on Neural Information Processing Systems,] (https://proceedings.neurips.cc/paper/2019/file/5103c3584b063c431bd1268e9b5e76fb-Paper.pdf) 2019. 



[6]Lakshminarayanan, Balaji, Alexander Pritzel, and Charles Blundell. ["Simple and scalable predictive uncertainty estimation using deep ensembles."] (http://papers.nips.cc/paper/7219-simple-and-scalable-predictive-uncertainty-estimation-using-deep-ensembles.pdf) 2017.





## Experimental Details

1. [property_of_learning_f](https://github.com/thuizhou/Collaborating-Networks/tree/main/property_of_learning_f): CN's stability under overparameterization, and the merit of learning g and f jointly over learning g alone with a fixed f. 
2. [synthetic_examples](https://github.com/thuizhou/Collaborating-Networks/tree/main/synthetic_examples): Two synthetic examples simulated from Gaussian and Weibull Distribution
3. [real_data](https://github.com/thuizhou/Collaborating-Networks/tree/main/real_data): Five real data examples.


Overall:

* CN has great recovery of the ground truth distribution in the synthetic examples:

[Gaussian Sample](https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/syn1dist1.pdf)

<p align="center">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-1/syn1TH1.png">
  <img width="400" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/synthetic_examples/syn-2/syn2TH2.png">
</p>


* CN has faithfull interval coverage(calibration)


<p align="center">
  <img width="700" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Airline/airc.png">
</p>


* CN increases the interval sharpness:
<p align="center">
  <img width="700" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/real_data/Energy/energyl.png">
</p>



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
