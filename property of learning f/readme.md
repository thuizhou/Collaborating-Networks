### This repository explores the property of learning f-Network

We set up a synthetic example to evaluate the impact of learning f in the finite sample case. 
We introduce three variantes of CN: 

>U-g: learning the distribution with g function alone with a uniform distribution on f
>T-g: learning the distribution with g function alone with f as the ground truth inverse cdf(practically impossible) 
>CN-g: learning the distribution with g function and f jointly(the normal setup of CN)


The folder 88888 simulate an overfitting example. We adopt an overparameterized neural network architectures, which creates an interpolating setting in a typically trained neural network.

\mlp_qr.ipynb: Describe the data generating process. Evaluation data saved as 888888.
This note book also illustrates that overfitting can easily happen by
estimating conditional mean with MSE, the conditional median (QR\_0.5),the conditional 25'th quantile (QR_0.25), and the conditional 75'th quantile (QR_0.75) estimated by the quantile regression

![calib](overfit_discover/calibration.png)

For the three variants of CN, they do not collapse to observed outcomes in all three cases.
By introducing the joint learning scheme, CN-g is obviously better than U-g in generating more faithfull and sharper intervals. 

\mlp_qr.ipynb: implementation of T-g
![calib](overfit_discover/calibration.png)


\mlp_qr.ipynb: implementation of U-g
![calib](overfit_discover/calibration.png)


\mlp_qr.ipynb: implementation of CN-g
![calib](overfit_discover/calibration.png)









