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

<p align="center">
  <img width="420" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/pt_mseqr.png">
</p>


For the four variants of CN, they do not collapse to observed outcomes in all three cases.
By introducing the joint learning scheme, CN-g is obviously better than U-g and CN-f in generating more faithfull and sharper intervals. 


Implementation of T-g:
[tg](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/Tg.ipynb): 

<p align="center">
  <img width="420" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gc.png">
</p>


Implementation of U-g:
[ug](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/Ug.ipynb): 

<p align="center">
  <img width="420" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gd.png">
</p>

Implementation of CN-g and CN-f
[cngf](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/CNgf.ipynb): 

<p align="center">
  <img width="420" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gfg.png">
</p>

<p align="center">
  <img width="420" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/overfit_discover/dist_gff.png">
</p>

### [convergence rate](https://github.com/thuizhou/Collaborating-Networks/tree/main/property_of_learning_f/convergence_rate) 
Use the same synthetic example to compare the convergence rate of the three variantes.


[tg_converge](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/Tg_converge.ipynb): implementation of T-g

[ugconverge](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/Ug_converge.ipynb): implementation of U-g


[cngfconverge](https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/CNgf_converge.ipynb): implementation of CN-g and CN-f

<p align="center">
  <img width="620" src="https://github.com/thuizhou/Collaborating-Networks/blob/main/property_of_learning_f/convergence_rate/conv.png">
</p>



