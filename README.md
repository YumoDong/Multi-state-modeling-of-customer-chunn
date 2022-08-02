# Multi-State-Modeling-of-Customer-Churn

This directory provides data and codes to reproduce the results in the following paper:

Multi-State Modelling of CustomerChurn

Software Dependency
===================
The plots/tables were produced under the following software
1. RStudio 2022.07.0+548 
2. Operating system: Windows 10

[Important Notes]:

1. There are three data sets named "LGPIF-LBD-ALL4-2006-10.csv", "LGPIF-LBD-ALL4-2011-14.csv" and "dataAugust2022.RData". The first two .csv files are the raw data sets of the LGPIF, while the last one is the processed data set that can be directly used to reproduce the paper. The code of processing raw data sets is saved in "DataProcessing_Multistate Customer Churn.rmd", in which there are detailed comments to help readers understand the data processing. 

2. "Paper Reproduction.rmd" contains the codes to reproduce all the results of the paper, and it directly uses "dataAugust2022.RData" at the beginning.

3. Please read the following Guidlines for Reproduction to see the details of reproducing the result in each section of the paper.

Guidlines for Reproduction
=========================
1. In "Paper Reproducation.rmd", there are several sections divided by #, which follow the order of the paper. There is normally one theme in each section, where there are many chunks that subdivide different differernt tasks. We have made lots of comments to the codes though there is no code being difficult to understand. If you do not use R Markdown, then you can copy the codes in each chunk to R Studio and run it.

2. Because tuning hyparameters for GBMs and SVMs is time-consuming, so we saved the tuned models: gbm_caret_ori2022.RData, gbm_caret_bal2022.RData, svm_caret_ori2022.RData and svm_caret_ori2022.RData. They represent the tuned GBM in the original training set, GBM in the balanced training set, tuned SVM in the original training set and SVM in the balanced training set. We also provide the code of parallel computing to speed up the tuning process. 

3. The random seed was set to be 2022. Changing the seed may lead to different parameters for machine learning models and a different balanced (oversampling )training set.

4. Feel free to contact this email if you have any question: yumo.dong@anu.edu.au
