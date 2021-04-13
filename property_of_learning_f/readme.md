## This repository explores the property of learning f-Network

We set up a synthetic example to evaluate the impact of learning f in the finite sample case. 
We introduce three variantes of CN: 

* U-g: learning the distribution with g function alone with a uniform distribution on f
* T-g: learning the distribution with g function alone with f as the ground truth inverse cdf(practically impossible) 
* CN-gf: learning the distribution with g function and f jointly(the normal setup of CN)


### [overfit_discover](https://github.com/thuizhou/Collaborating-Networks/tree/main/property_of_learning_f/overfit_discover) 
simulates an overfitting example. We adopt an overparameterized neural network architectures, which creates an interpolating setting in a typically trained neural network.

[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/tree/main/property_of_learning_f/overfit_discover): Describe the data generating process. Evaluation data saved as xymusd.npy.
This note book also illustrates that overfitting can easily happen by
estimating conditional mean with MSE, the conditional median (QR\_0.5),the conditional 25'th quantile (QR_0.25), and the conditional 75'th quantile (QR_0.75) estimated by the quantile regression
![mse](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/pt_mseqr.png)

For the four variants of CN, they do not collapse to observed outcomes in all three cases.
By introducing the joint learning scheme, CN-g is obviously better than U-g and CN-f in generating more faithfull and sharper intervals. 

[tg](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/Tg.ipynb): implementation of T-g
![tgplot](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gc.png)


[ug](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/Ug.ipynb): implementation of U-g
![ugplot](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gd.png)


[cngf](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/CNgf.ipynb): implementation of CN-g and CN-f
![cngplot](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gfg.png)

![cnfplot](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gff.png)


### [convergence rate](https://github.com/thuizhou/Collaborating-Networks/tree/main/property_of_learning_f/convergence_rate) 
Use the same synthetic example to compare the convergence rate of the three variantes.


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/Tg_converge.ipynb): implementation of T-g

[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/Ug_converge.ipynb): implementation of U-g


[mlp_qr.ipynb](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/CNg_converge.ipynb): implementation of CN-g

[Overall convergence rate](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/conv.pdf)


