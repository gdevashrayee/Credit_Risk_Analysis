# Credit_Risk_Analysis
Using scikit-learn and imbalanced-learn to analyze sample credit data for credit risk.


## Overview
The aim of this investigation was to develop and assess alternative machine learning models to assess the credit risk of each individual consumer. The dataset from LendingClub, "a peer-to-peer loan services company," was utilized to train the models. The dataset had 68,817 entries after cleaning, and just 0.5 percent of these were considered to be "high risk." It was also severely imbalanced.
![Overview](images/one.png)

The machine learning algorithms used were:
* RandomOverSampler
* SMOTE
* ClusterCentroids
* SMOTEENN
* BalancedRandomForestClassifier
* EasyEnsembleClassifier

The models were run, and their efficacy at forecasting credit risk was then assessed.

## Results
We will look at the Balanced Accuracy Score and the Imbalanced Classification Report (ICR) from each model when analyzing the findings. Since we're particularly interested in our capacity to identify high credit risk individuals, two figures from the "f1" (F-score) column—the number from the bottom "avg / total" row and the f-score from the "high risk" row—are of special relevance in the ICR.

Based on their Balanced Accuracy Scores, the results below are presented in descending order of performance, starting with the model that performed the poorest and working up to the best.
* The least accurate method, **Cluster Centroids** Undersampling, produced results of 0.5295. That indicates that its accuracy in anticipating credit risks was little better than 50%, or a coin toss. 
![Two](images/two.png)

Its F-scores were also unimpressive, coming in at only 0.56 on average and 0.01 for high-risk prediction.
![Three](images/three.png)

* The second-worst results were from **Combination Sampling**, with an accuracy rating of 0.6529. This suggests that its accuracy in anticipating credit risks was just slightly above 65%, or 2/3 of the time.
![Four](images/four.png)

Its F-scores were nevertheless poor, coming in at only 0.72 on average and 0.02 for high-risk prediction.
![Five](images/five.png)

* With an accuracy score of 0.662, **SMOTE Oversampling** produced the third-worst outcomes for us. This performance is comparable to that of **Combination Sampling**. This indicates that its accuracy in anticipating credit risks was only slightly above 66 percent, or 2/3rds.
![Six](images/six.png)

Its F-scores were likewise poor, with a 0.80 average improvement on the previous F-score and a 0.02 F-score for high-risk prediction.
![Seven](images/seven.png)

* We have reached the halfway point of our model performances thanks to **Naive Random Oversampling**. We received the third-best results from the ROS model, which had an accuracy rating of 0.6732. This performance is still comparable to what we observed using combination sampling and SMOTE oversampling. This indicates that its accuracy in anticipating credit risks was only slightly above 67 percent, or 2/3rds.
![Eight](images/eight.png)

Also worse or comparable to **SMOTE Oversampling** were its F-scores. The average score for the ROS model was 0.76, and the F-score for high-risk prediction was only 0.02.
![Nine](images/nine.png)

* With an accuracy score of 0.7615, the **Balanced Random Forest Classifier** provided us with the second-best results. This is still far from ideal, though. This suggests that only roughly 76% of the acceptable levels of credit risks might be effectively predicted.
![Ten](images/ten.png)

Where there was the most improvement was in its F-scores (relatively). The average F-score for the BRFC model was 0.92, which is at least in the 90s. Its F-score for high-risk prediction was only 0.06, which is still very low.
![Eleven](images/eleven.png)

* **Easy Ensemble AdaBoost Classifier**, the model that performed the best overall was AdaBoost Classifier**. The outcomes much beyond those of any other models that had been tried. We received a score of 0.9319 for accuracy. This indicates that, despite imperfections, it could correctly anticipate the right levels of credit risks at a rate of more than 93%.
![Twelve](images/twelve.png)

Its F-scores were likewise rather good. The average F-score for the EEC model was 0.97. Even though it was the best performing, it still had a poor F-score for high-risk prediction—only 0.16.
![Thirteen](images/thirteen.png)

## Summary
In conclusion, even for sophisticated machine learning algorithms with 93 columns of data to analyse, credit risk is a challenging thing to anticipate. The dataset was incredibly imbalanced, which is largely why the **Easy Ensemble AdaBoost Classifier** model achieved the highest overall accuracy. Its average F-score and balanced accuracy were both above 90%, while its F-score for high-risk predictions was only 0.16. Finally, I would advise against utilizing any of these algorithms because doing so would put creditors at undue danger because they wouldn't be able to foresee who the high-risk customers or debtors would be.