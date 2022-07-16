## Credit_Risk_Analysis

### Overview   
The purpose of this analysis is to identify the best model to predict high-risk loans for LendingClub, a peer-to-peer lending services company.  The goal of the lender is to minimize or eliminate high-risk loans by using machine learning to predict which loans will classified as high-risk using 86 variables related to credit history and other relevant characteristics.  This project determines the best model to fit the organization’s needs and makes a recommendation.  

The loan company processes and issues hundreds of thousands of applications in a quarter.  Machine learning algorithms are the most effective means of conditioning loan acceptance for this industry.  Because the goal is to maximize the number of loans identified as high risk, a model which prioritizes sensitivity is the most appropriate.  This analysis considers nine (9) different models, ranking each.  

### The Dataset  
The dataset comprises information for loans for the first quarter 2019.   It consists of 688,017 samples categorized into high risk and low risk.  Over 99 percent of the samples fall into the low-risk category, leaving the remaining less-than-one percent in the high-risk population.  This population is the target class and is treated as the positive class in the models.  

![image](https://user-images.githubusercontent.com/101474477/179372582-b58f8ae2-da49-47be-abbd-3778f6dbdd21.png)



### The Analysis  
With such an extremely unbalanced dataset, it is necessary to use a model that is structured to compensate for imbalance.  The models assessed here include oversampling (Naïve Random Oversampler and SMOTE); undersampling (ClusterCentroids); combination (SMOTEENN), and ensemble (Balanced Random Forest Classifier, Easy Ensemble ADAboost Classifier, Random Forest Classifier, RUS Boost Classifier, and Bagging Classifier).  

Because the target, high-risk, is the minority class, this analysis focuses attention on the sensitivity metric instead of on precision.  Sensitivity is the measure of the percentage of true positives calculated as a part of all the samples the model classified into the positive category.  This metric ensures that all true positives are captured in the model, and is used when identifying positive samples is of absolute importance.  Sensitivity, for example, is the definitive consideration in diagnostic protocols, where identifying the ill patients as ill is a greater priority than mis-identifying healthy patients as ill.   The trade-off here is between sensitivity and precision, which looks at how many samples predicted as positive actually are positive. The objective for the loan services company is to ensure all high-risk loans are classified as such, rather than ensuring the accuracy of those that are already included in the positive class.  Casting a broader net of positives increases the odds of catching all those that should be included.  

### Metrics  
With a very small target relative to the non-target class, the analysis draws conclusions using the metrics of the target class rather than the total or average metrics for the model.  A model can have very high scores overall, but very low scores for the target for those same metrics.  This simply means that the model’s algorithm process leaned into the majority class.  Models with high, even distributions between the minority class results and the total results for the models are successful.  

### Analysis  
The metrics used to define success in the analysis included sensitivity, the f1 score, and the balanced accuracy score.  Other metrics generated and reviewed in the course of the project included precision, specificity (the true negative rate), and the indexed balanced accuracy score.  Output was generated in the form of the balanced accuracy score, confusion matrices, and imbalanced classification reports.   

### Results   

![image](https://user-images.githubusercontent.com/101474477/179372405-0567c5ee-afc1-449e-9cf3-5c87973388f4.png)

 	 	

Based on the grid above, the Easy Ensemble Adaboost classifier is the best predictor for this project, followed by SMOTEENN.  The Balanced Random Forest Classifier is also an effective model as it appropriately treats the high-risk class.
 
### Output   
 
 ![image](https://user-images.githubusercontent.com/101474477/179372490-e746a6c3-1116-4dc4-92cc-e169770825a3.png)

Adaboost Easy Ensemble

 ![image](https://user-images.githubusercontent.com/101474477/179372542-433e1f8f-2bfe-4465-ba48-6c7f721a8095.png)

SMOTEENN
 
 ![image](https://user-images.githubusercontent.com/101474477/179372562-263efcff-f5d2-4156-affe-488cd5433246.png)

Balanced Random Forest
