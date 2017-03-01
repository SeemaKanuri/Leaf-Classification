# Leaf Classification

# Problem Discussion

All leaves have different characteristics which can be used to create a classification system. Classifying the plants based on its leaves can be helpful way to begin researching plant types. Where classification here it meant systematic grouping, or arranging of things into categories based on similar features and characteristics. Here I aimed to identity the leaf based on their unique characteristics to distinguish the various plant species. Using the binary leaf images and extracted features, including shape, margin & texture I aim to identify the 99 species of plants available to us.

# Significance

Identifying a plant species by its leaves will be very helpful in tracking the species population and preservation. Also, it helps in food supply management apart from carrying out the plant based medicinal research. For instance, identifying the leaf structure can provide more broader insight in the way to preserve and track the population of it.

# Data Preparation and Feature identification

All images are converted to binary black leaves and provided with three sets of features for the given 1584 images are a shape contiguous descriptor, an interior texture histogram, and a ﬁne-scale margin histogram. Each image is identified with a unique value which is named as ‘ID’ from 1 to 1548.

Missing Values

Considering the datasets this shows that the dataset is complete and there is no need of doing to clean it from empty entries’. there is no Null value of feature shape, texture and margin in the given dataset.

# Type of Models

I performed in various classification process using the train and test dataset. In this I have sued neural networks, random forest and multinomial regression over it has been determined that multinomial regression has good accuracy with an approximate model score of multinomial regression is 0.0101.

# Neural Network

Neural networks can solve pattern recognition problems and with enough elements (called neurons) can classify any data with arbitrary accuracy. They are particularly well suited for complex decision boundary problems over many variables. Therefore, I have chosen neural networks and Neuroph Studio as a good candidate for solving the classification problem represented below.
I used a 4-layer network but it resulted in overfitting the test set. So, by dropping the count of neurones and I submitted each sample as a probabilistic distribution over all the possible outcomes. This has reduced the multiclass log loss.

# Multinomial Regression

Multinomial logistic regression is used to model nominal outcome variables, in which the log odds of the outcomes are modeled as a linear combination of the predictor variables. In python, I have used scikit learn package to perform multinomial regression.
In statistics, multinomial logistic regression is a classification method that generalizes logistic regression to multiclass problems, i.e. with more than two possible discrete outcomes. That is, it is a model that is used to predict the probabilities of the different possible outcomes of a categorically distributed dependent variable, given a set of independent variables (which may be real-valued, binary-valued, categorical-valued, etc.). In multinomial regression, I have scored better as compare to other models. By further enhancing the model I have tuned the parameters and scores better using the tuned parameter. By applying the multinomial regression, I have (Kaggle  competition score)  scored 0.02139 which is under top 10% of the total scores (Kaggle  competition).

# Random Forest

andom forests are a notion of the general technique of random decision forests that are an ensemble learning method for classification, regression and other tasks, that operate by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.
When I have used random forest model in the random forest I have taken various parameters to tune the performance, however after tuning the parameters the score is limited and there are very less chances to improve. So, that’s why I have dropped random forest. By using random forest, I have (Kaggle competition score) scored 0.70052. By further enhancing the parameter I have faced the issue of overfitting the models which cause even more depletion in performance.


# Formulation 

Each leaf specimen is converted into binary black leaves with white background. Binary versions are provided for simple leaves. I have used several libraries to analyze text as well as image Information. In Text file named train and test I have margin, shape and texture where as in image I should extract features from the different images based on different features.
I have used several libraries to compute and to extract features from the image as well as from the text file. 

cv2
Numpy
Pandas
Label Encoder
StandardScaler
Model Performance

I have Enhanced the model performance from (Kaggle  competition score) 1.80485 to 0.02139 by adding several features and by tuning the parameters. 

# Limitations

Features Extraction

Limited features can be extracted from the images as the image is gray scale.

Complexity

By adding more features to the Data caused the code and time complexity due to which the performance has several limitations. 

Kaggle Limitations

In leaf classification, I have limited upload of the submission file as due to which much more experiments are limited.

# Learning

I have got the more exposure to various algorithms and classifiers, I have learned to tune parameters and learned to extract image features like area, perimeter, aspect ratio, extent, contour, diameter of the image. Also learned about the batch size while dealing with Neural Networks. Understood how the deeper networks works for the image classification compared to shallow networks. Also, I have generated the submission file based on the probability which is yet another challenge, also I must transform the Data Frame to scaler arrays due to which the model is tuned and helps us to get better understanding of the models.
