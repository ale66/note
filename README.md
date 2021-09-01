# NOTE: Non-parametric Oversampling Techniques for Explainable Credit Scoring

This repository is ancillary to the eponymous submission to pVLDB.

The available [HMEQ public dataset](https://github.com/ale66/note/blob/main/hmeq.csv) is for validation purposes.

The [Jupyther-style notebook](https://github.com/ale66/note/blob/main/note.jpynb) has been designed by [Seongil Han](https://www.dcs.bbk.ac.uk/about/people/research-students/han-seongil/)

## What it does
Imbalanced classes, i.e., a disproportionate ratio of observations in each class, are a common issue in the Machine Learning classification for credit scoring. 
Although Synthetic Minority Oversampling TEchnique (SMOTE) has been the most widely used to oversample the minority class, its performance is still not reaching the acceptable level as neighboring examples which can be from other classes are not taken into consideration. 
It also performs poorly when data is high-dimensional and non-linear. When the overlapping of classes is increased, it can introduce additional noise. 
As an alternative, Generative Adversarial Networks (GAN) has recently gained popularity. 

GANs generate synthetic distribution after learning original data which makes it capable to model complex and non-linear distributions. 
Several recent studies based on conditional Wasserstein GANs (cWGANs) have shown robust performance in modelling tabular data for credit scoring with both numerical and categorical features. 
A limited number of studies, however, have been conducted on extracting latent features from non-linear credit scoring data and the existing studies have not considered the explainability aspect for credit scoring models. 

NOTE proposes a novel oversampling technique named NOTE (Non-parametric Oversampling Techniques for Explainable Credit Scoring) to overcome such limitations. 
NOTE consists of three main components. 

* First, non-parametric stacked autoencoder (NSA) extracts latent features that contain non-linear features. 

* Second, a cWGAN is utilised to oversample the minority class. 

* Third, using the re-constructed balanced dataset with latent features, the credit scoring classification considering the explainable ML aspect is performed. 

Our experimental results successfully demonstrated the utility of the novel concepts used in NOTE by outperforming the state-of-the-art oversampling methods by improving the classification accuracy by 3.8\% with Gradient Boosting, 11.6\% with Decision Trees and 17.1\% with Logistic Regression. 
This could also lead to a better model explainability and the stability particularly for non-linear credit scoring dataset. 

