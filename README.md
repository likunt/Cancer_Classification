# Cancer_Classification

This project aims to  identify the probable cause of cancers in terms of genes responsible for different types of cancers, such as breast cancer, renal cancer, colon cancer, lung cancer, and prostate cancer. This would lead us to early identification of each type of cancer reducing the fatality rate. Original data source: https://archive.ics.uci.edu/ml/datasets/gene+expression+cancer+RNA-Seq#

#### Dataset Details:
The input dataset contains 801 samples for the corresponding 801 people who have been detected with different types of cancer. Each sample contains expression values of more than 20K genes. Samples have one of the types of tumors: 
* BRCA (Breast cancer)
* KIRC (Kidney renal clear cell carcinoma)
* COAD (Colon adenocarcinoma)
* LUAD (Lung adenocarcinoma)
* PRAD (Prostate adenocarcinoma)

### Conclusion

In this study, we aim to identify different cancer types based on expression count of 20K genes. 
- By performing dimensionality reduction on the high dimensional gene space, we found that samples are well seperated even in a 2d space. Among the dimensionality reduction techniques, t-SNE performs best, followed by LDA and PCA.
- We then applied different clustering methods such as K-Means, Gaussian Mixture and DBSCAN on t-SNE reduced feature space (K-Means applied on the full space), both Gaussian Mixture and DBSCAN success in clustering samples with same cancer type in the same cluster, with only 1 mislabeled sample. It is expected as we have well seperated dataset in reduced feature space.
- We then built classification models using SVM, random forest and neural net. We found the SVM obtained a high test arrcuracy of almost 100% with a relatively high efficiency.
- Lastly, we selected features based on PCA, forward selection and ANOVA test and trained the classifiers on the three sets of selected features seperately. In all the tests, the time efficient has been improved by 100 times without degrading the test accuracy.
