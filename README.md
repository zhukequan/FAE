# FAE

Feature Analysis Explorer (FAE) can help researchers develop a classification model with comparison among different methods. This project was inspired on the [Radiomics](http://www.radiomics.io/), and provides some functions to help extract features with batch process.



If you publish any work which uses this package, I will appreciate that you could cite the following publication: [Song Y, Zhang YD, Yan X, Liu H, Zhou M, Hu B, Yang G, Computer-aided diagnosis of prostate cancer using a deep convolutional neural network from multiparametric MRI. J Magn Reson Imaging. 2018 Apr 16. doi: 10.1002/jmri.26047.](https://www.ncbi.nlm.nih.gov/pubmed/29659067) 

Welcome any issues and PR. 

![Python](https://img.shields.io/badge/python-v3.6-blue.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-GPL3.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.en.html)

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisties
The below modules must be installed first to make the FAE work. 

```
- pyradiomics
- pandas
- numpy
- scikit-learn
- scipy
- matplotlib (seaborn)
- PyQt5
```

### Installing
Just clone it by typing in:

```
git clone https://github.com/salan668/FAE.git
```
If you would like to use FAE in any project, please add the path in your system envirement. A trick method is to create a .pth file in the site-packages folder (<Your own python folder>\Lib\site-packages) and add a path that point to the root folder of the FAE.

### Running the example. 
**TODO**

### Architecture of Project 
- **DataContainer**
    - **DataContainer**. The structure to contain the data, which also includes methods like saving/loading.
    - **DataSeparate**. Including functions to separate data into training part and testing part.
    - **DataBalance**, The class to deal with data imbalance. Now we provided Under-sampling, Over-sampling, and SMOTE method.
- **Feature Analysis**
    - **Normalization**. To Normalize the data
    - **DimensionReduction**. To reduce the dimension, including PCA. 
    - **Classifier**. The classifier to develop the model, including SVM, AE, Random Forests, LDA. 
    - **CrossValidation**. The CV model to estimate the model. Return the metrics
    - **FeatureSelector**. The class to select features, which including 1) remove non-useful features, e.g. the VolumnNum; 2) different method to select features, like ANOVA, RFE, Relief.
    - **FeturePipeline**. The class to estimate the model with different feature selected method and classifier. 
- **Image2Feature**
    - **RadiomicsFeatureExtractor**. This class help extract features from image and ROI with batch process. This class should be more "smart" in the future. 
- **Visulization**. 
    - **DrawDoubleLine**. This function helps draw doulbe-y plot. e.g. plot accuracy and error against the number of iterations.
    - **DrawROCList**. This function helps draw different ROC curves. AUC will be calculated automaticly and labeled on the legend. 
    - **FeatureRelationship**. This function helps draw the distribution of the values of different features. I can only show at most 3 features in one figure. 
    - **FeatureSort**. This function helps draw the features and the weights of them on the classifiction model. 
    - **PlotMetricVsFeatureNumber**. This function helps draw the AUC / Accuracy / other metrics against the number of chosen features. This can help find the adaptive number of the features. 

## Document
TODO

## Author
- [**Yang Song**](https://github.com/salan668)

## License 
This project is licensed under the GPL 3.0 License - see the [LICENSE.md](https://github.com/salan668/FAE/blob/master/LICENSE) file for details

## Acknowledge
- Contributor:
    - [**Guang Yang**](https://github.com/yg88)
    - Yi-lai Pei
    - Jing Zhang
    - [**jmtaysom**](https://github.com/jmtaysom)
- Demo data support. 
    - Yu-dong Zhang, Xu Yan. 
