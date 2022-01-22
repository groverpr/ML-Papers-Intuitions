


#### [In Defense of Pseudo-Labeling: An Uncertainty-Aware Pseudo-label Selection Framework for Semi-Supervised Learning](https://openreview.net/pdf?id=-ODN6SbiUU)

> *Conference: ICLR 2021 | Authors: Mamshad Nayeem Rizve, Kevin Duarte, Yogesh S Rawat, Mubarak Shah*

> **Brief background:** 
    Pseudo Labeling (PL) is a semi supervised learning (SSL) approach in which you iteratively train supervised model using labels + pseudo labels. Pseudo labels are generated from the unlabeled data that have high prediction score (above a certain cut-off). In SSL literature, PL is generally beaten by techniques that use domain specific data augmentations for learning patterns from unlabeled data. Data augmentations work great in SSL, but can’t be done for all types of data, e.g. tabular data. Pseudo labeling does not rely on data augmentations and are more generic. The technique in this paper attempts to bridge the gap b/w data augmentation based SSL vs. pseudo labeling.

> **Key idea:** 
    Main idea behind this paper is to use the uncertainty of predictions from the test data as additional information before selecting pseudo labels. Uncertainty of a prediction can be found in neural network by applying dropout during test time and generating prediction for the same input N times. The standard deviation from N predictions (on same input) is used as uncertainty measure.  

> **Important equation to understand:**

> **One result worth mentioning:** 

