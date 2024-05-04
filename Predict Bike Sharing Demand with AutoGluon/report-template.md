# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Aya Bakr

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
It was discovered that several of the forecasts had negative values when the initial submission attempt was made. Submissions with negative forecasts are rejected by Kaggle. Consequently, prior to presenting the results, all negative predictions have to be set to zero. With this modification, Kaggle's requirements were met, enabling the findings to be successfully submitted for assessment.

### What was the top ranked model that performed?
The top ranked model that performed in the AutoGluon training was the WeightedEnsemble_L3 model. This model achieved the best performance among all the models tested during the training process.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The distribution and connections between the variables in the dataset were made clear using the exploratory data analysis (EDA). Furthermore, it was noted that the demand for bike sharing was significantly influenced by the hour of the day. New characteristics including year, month, day, and hour were taken out of thedatetime column in order to make use of this data. In order to capture temporal patterns and give the predictive model more data to enhance its performance, several extra characteristics were developed.

### How much better did your model preform after adding additional features and why do you think that is?
The model's performance greatly increased with the addition of new features that were obtained from the datetime column. The original model received a Kaggle score of 1.80, whereas the feature-added model received a score of 0.72. The reason for the improvement is that the new features have improved the depiction of temporal patterns they have captured. The model was able to better comprehend how the demand for bike sharing changes over time by adding data about the year, month, day, and hour. Better predictions were produced by the model's ability to identify more subtle patterns in the data thanks to the temporal characteristics' better resolution. All things considered, the inclusion of these features improved the model's performance by enriching its input space.


## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model's performance significantly improved following the application of hyperparameter tuning (HPO) and several hyperparameter experiments. The model trained with HPO obtained a substantially lower Kaggle score of 0.49, while the original model obtained a score of 1.80. The enhancement can be credited to the model's hyperparameters being optimized, which improved the model's ability to match the data. The model was able to improve its generalization performance on untested data by methodically going through the hyperparameter space and choosing the best combination. Predictive accuracy increased as a result of the model's architecture and configuration being optimized through this fine-tuning procedure. Overall, improving the model's performance and lowering prediction error was greatly aided by hyperparameter adjustment.


### If you were given more time with this dataset, where do you think you would spend more time?
I would look into other features that might be able to extract more intricate relationships from the data. This could entail experimenting with various transformations of current features to increase their prediction value or developing new features based on domain expertise.  In order to determine whether more improvements in predicted accuracy may be made, I would examine the effectiveness of various machine learning algorithms and ensemble techniques. Utilizing ensemble strategies, like stacking or combining several models, may help to maximize the benefits of various methods and enhance performance as a whole.
 Even though hyperparameter tuning was done, a wider range of hyperparameters could still be explored through more thorough grid or random search. This may result in the identification of more effective combinations that enhance model performance.


### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|Initial|Default values|Default values|Default values|1.80|
|Add_features|Default values|Default values|Default values|0.72|
|hpo|GBM: num_leaves: lower=26, upper=66|XGB: max_depth lower=5, upper=9|refit_full='best'|0.49|


### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.
(attached in the file)
### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

(attached in the file)

![model_test_score.png](img/model_test_score.png)

## Summary
The goal of this research was to use the automated machine learning package AutoGluon to create a forecast model for bike-sharing demand. By means of data preparation, exploratory analysis, and feature engineering, the dataset was enhanced in terms of its input space for the model by obtaining insights into temporal trends. The model's performance was further enhanced by hyperparameter tuning, which led to a notable decrease in the Kaggle score to 0.49. When compared to baseline models, HPO's effectiveness in raising prediction accuracy was highlighted. Further investigation into feature engineering, model selection, and validation techniques could potentially improve model performance and practicality in the future.
