# breast_cancer_classification
Predicting whether the tumor is Malignant or Benign using Machine Learning on the UCI-Wisconsin data set

### Summary

> National Breast Cancer Foundation estimates that 1 in 8 women in the U.S. will develop breast cancer in her lifetime. For fine-needle aspiration biopsy(FNAB), the pathology report alone could take up to 2 weeks, with an accuracy of about 80% [1,2](https://github.com/floraxinru/breast_cancer_classification/blob/master/README.md#references). 

For this 2.5-week project, I trained and compared 9 classification models to predict breast cancer using features already calculated from biopsy images. The objective is to investigate whether it is possible to improve the accuracy and speed of the diagnosis using machine learning.

My prediction results were very good (AUC ~ 0.99 for top 4 models, compared to human accuracy of 77.5%), and the natural next step would be to expand the problem to include image classification on biopsy images, and calculating the features before performing classification using the best model I trained. 

### *Tools*
Python, Pandas, NumPy, scikit-Learn, matplotlib, seaborn

### Design
Learning from previous projects, I deliberately cut down on project design and data collection time for this project, and narrowed down the scope, in order to perform a more thorough analysis on the results, and spend time building a data story.

### Data
The dataset has 33 features, 569 observations. My target feature for classification is the Diagnosis (M = malignant, B = benign). To predict the diagnosis, I used these ten computed features:

  * radius (mean of distances from center to points on the perimeter)
  * texture (standard deviation of gray-scale values)
  * perimeter
  * area
  * smoothness (local variation in radius lengths)
  * compactness (perimeter^2 / area - 1.0)
  * concavity (severity of concave portions of the contour)
  * concave points (number of concave portions of the contour)
  * symmetry
  * fractal dimension ("coastline approximation" - 1)


### Results

### Future Work
To continue working on this and expand it to include image classification, I would first look into the papers that cited this dataset (linked on the UCI data source), to see what image data they used. I would also check those papers to see if there are now more advanced models used to calculate these features from biopsy images, before trying to repeat the calculation to get geometric features similar to the ones I used in this dataset.

### References
1. https://www.nationalbreastcancer.org/breast-cancer-biopsy
2. https://www.ncbi.nlm.nih.gov/pubmed/21829998
