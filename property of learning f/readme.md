## This repository explores the property of learning f-Network

We set up a synthetic example to evaluate the impact of learning f in the finite sample case. 
We introduce three variantes of CN: 

* U-g: learning the distribution with g function alone with a uniform distribution on f
* T-g: learning the distribution with g function alone with f as the ground truth inverse cdf(practically impossible) 
* CN-g: learning the distribution with g function and f jointly(the normal setup of CN)


### [overfit_discover](https://github.com/thuizhou/Collaborating-Networks/tree/main/property%20of%20learning%20f/overfit_discover) 
simulates an overfitting example. We adopt an overparameterized neural network architectures, which creates an interpolating setting in a typically trained neural network.

[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/tree/main/property%20of%20learning%20f/overfit_discover): Describe the data generating process. Evaluation data saved as xymusd.npy.
This note book also illustrates that overfitting can easily happen by
estimating conditional mean with MSE, the conditional median (QR\_0.5),the conditional 25'th quantile (QR_0.25), and the conditional 75'th quantile (QR_0.75) estimated by the quantile regression
[Result](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/pt_mseqr.pdf)

For the three variants of CN, they do not collapse to observed outcomes in all three cases.
By introducing the joint learning scheme, CN-g is obviously better than U-g in generating more faithfull and sharper intervals. 

[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/Tg.ipynb): implementation of T-g
[Result](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/dist_gc.pdf)


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/Ug.ipynb): implementation of U-g
[Result](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/dist_gd.pdf)


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/CNg.ipynb): implementation of CN-g
[Result](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/overfit_discover/dist_gf.pdf)


### [convergence rate](https://github.com/thuizhou/Collaborating-Networks/tree/main/property%20of%20learning%20f/convergence%20rate) 
Use the same synthetic example to compare the convergence rate of the three variantes.


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/convergence%20rate/Tg_converge.ipynb): implementation of T-g

[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/convergence%20rate/Ug_converge.ipynb): implementation of U-g


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/convergence%20rate/CNg_converge.ipynb): implementation of CN-g

[Overall convergence rate](https://github.com/thuizhou/Collaborating-Networks/blob/main/property%20of%20learning%20f/convergence%20rate/conv.pdf)


