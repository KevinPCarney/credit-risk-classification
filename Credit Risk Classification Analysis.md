# Module 20 Report

The work in this repository, was done for the credit-risk-classification assignment.  It was intended to be a method to explore the use of machine learning as it would likely appear in a professional setting.  Our data originated from the "lending-data.csv" that was provided as part of the instructions. The data set itself was made up of  77,536 lines of data that analized a number of characteristics to include loan size, interest rate, and borrower income amongst others.  The objective was to take this data and train an algorithm based on it.  From there we would send this data through the various machine learning algorithms, and try and predict whether a potential borrower would risk having their loan enter into a default state, otherwise classified as a "high risk loan."  

Activity began by reviewing the data to see if supplemental cleaning was required.  All in all, the data only had numeric values and didn't appear to have nulls.  Also, given that there were a number of factors that could be used to determine the status of a loan, no columns were dropped or changed in any way.  That stated, there was a standard scaler that was applied.  This was particluarly notable in the "total_debt", "loan_size," and "borrower_income" had pretty large ranges.  After that, the "loan_status" values were counted and it was noted that there was significant imbalance in the values for whether a loan was in a good or default state, 75036 loans were in good standing, with only 2500 loans in default.  While this doesn't invalidate the effectiveness of the model, it does tend to be less effective.

A function called "doClassification" was created that formed the basis of the various algorithms that were ultimately applied.  This also created a Confusion Matrix, and plotted the Receiver Operating Characteristic (ROC) Curve.  From there, coding was employed to apply different machine learning algorithms to the data.  To include (but not limited to) Linear Regression, Randomforest, K Nearest Neighbor, and Ada Boost.  Each of these results were analyzed to measure their "Precision", "Recall", and "F1-Score," all of which are relevant to determining the best fit for the model.

The various algorithms had the following results: (Note: The % values below are associated with the accuracy of the model)

    Linear Regression: Precision - 87%, Recall - 98%, F1-Score - 92%
    Decision Tree Classification: Precision - 87%, Recall - 81%, F1-Score - 84%
    RandomForest: Precision - 88%, Recall - 88%, F1-Score - 88%
    Support Vector Classifier (SVC): Precision - 87%, Recall - 100%, F1-Score - 93%
    K Nearest Neighbors (KNN): Precision - 87%, Recall - 99%, F1-Score - 93%
    Extra Trees: Precision - 87%, Recall - 83%, F1-Score - 85%
    Adaptive Boosting (ADA): Precision - 87%, Recall - 99%, F1-Score - 93% 
    Gradient Boosting: Precision - 87%, Recall - 99%, F1-Score - 93%
    Extreme Gradient Boosting (XGB): Precision - 87%, Recall - 99%, F1-Score - 93%
    Light Gradient Boosting: Precision - 87%, Recall - 99%, F1-Score - 93%
    
Of the above algorithims, the ones that were the most effective were Adaptive Boosting, K Nearest Neighbors, and Extreme Gradient Boosting. Each of these had 93% accuracy.  That stated, for Extreme Gradient Boosting it had 90 False Positives and, 4 False Negatives, making it the overall best peforming model.  The other algorithms with 93% accuracy, each had 90 False Positives, and 5 False Negatives.  That stated, this is a comparatively limited sample size based on  other datasets used for machine learning.  This paired with the heavy imbalance of the data makes these models less useful in the long run.  While they might provide some valueable insights, and thus be worth running, the actionable intel is limited.

