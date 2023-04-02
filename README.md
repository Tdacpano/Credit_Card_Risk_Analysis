Credit Card Risk Analysis- Overview

   In this analysis we used a credit card credit dataset from LendingClub, and applied unsupervised learning by oversampling the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. We then use a combinatorial approach of Over- and Undersampling using the SMOTEENN algorithm. Followed by comparing two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

# Results: 
   After running each regression classifer on the data we were able to evalute each model's performance by calculating each accuracy score, generating a confusion matrix, and printing out each imbalanced classification report as provided below. In the deliverables below we evaluated three machine learning models by using resampling to determine which is better at predicting credit risk. We used the oversampling RandomOverSampler and SMOTE algorithms, and then used the undersampling ClusterCentroids algorithm.  

# Deliverable 1: Resampling Models

# RandomOverSampler:
<img width="297" alt="Screen Shot 2023-04-02 at 10 18 52 AM" src="https://user-images.githubusercontent.com/117120227/229368522-d477d6a2-689b-4855-a0c5-589a9d86f597.png">

<img width="561" alt="Screen Shot 2023-04-02 at 10 01 23 AM" src="https://user-images.githubusercontent.com/117120227/229367618-fdab2087-7ae2-4275-aba5-4c97e8468228.png">
   
   Taking a look at the RandomOverSampler classifier we can see that it has balanced accuracy score of around 64%. The high_risk precision is about 1% only with a 62% recall which makes the F1 score around of only 2%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100% with a recall of 68% and a F1 score of 76%. 


# SMOTE:
<img width="239" alt="Screen Shot 2023-04-02 at 10 23 57 AM" src="https://user-images.githubusercontent.com/117120227/229368796-a8f648ae-af9b-486d-bd40-7926d6db0395.png">

<img width="561" alt="Screen Shot 2023-04-02 at 10 01 52 AM" src="https://user-images.githubusercontent.com/117120227/229367641-73c1535a-68aa-4e6e-a4f0-7fed40aec144.png">
   
   Taking a look at the SMOTE classifier we can see that the results are similar to above with a balanced accuracy score of around 65%. The high_risk precision is still about 1% only with a 61% recall making the F1 score still around of only 2%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100% with a recall of 69% and a F1 score of 81%. The SMOTE model was slightly higher then the RanndomOverSampler model, but both produce nearly the same results. 
   
# ClusterCentroids:
<img width="297" alt="Screen Shot 2023-04-02 at 10 26 37 AM" src="https://user-images.githubusercontent.com/117120227/229368932-d2fcbe97-d765-4995-a473-488362ea5c26.png">

<img width="561" alt="Screen Shot 2023-04-02 at 10 02 11 AM" src="https://user-images.githubusercontent.com/117120227/229367654-b06495e3-5f75-4528-8431-e80be42ff93a.png">

   Next, we take a look at undersampling the data using the ClusterCentroids classifier. We can see in this model that the balanced accuracy score is lower then above with around 54%. The high_risk precision is still about 1%, with a 69% recall, making the F1 score still around of only 1%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100%, but with a much lower recall of 40% and a F1 score of 57%. The ClusterCentroids model came back with quite a bit lower numbers then the Oversampling models above.

# Deliverable 2: SMOTEENN Algorithm
<img width="297" alt="Screen Shot 2023-04-02 at 10 30 35 AM" src="https://user-images.githubusercontent.com/117120227/229369120-f5fb50ae-640c-4f0f-b817-6eb13e19b10d.png">

<img width="561" alt="Screen Shot 2023-04-02 at 10 02 54 AM" src="https://user-images.githubusercontent.com/117120227/229367684-e200299e-b149-453f-be5e-f73919ba928f.png">
   
   Next we combined both OverSampling and UnderSampling using the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms. We can see in this model that the balanced accuracy score is around 64%. The high_risk precision is still about 1%, with a 72% recall, making the F1 score still around 2%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100%, with recall of 57% and a F1 score of 72%. The SMOTEENN model came back with results that were a bit similar to the OverSampling models then the ClusterCentroids model. 
# Ensemble Classifers
  We continued our analysis by training and comparing two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. 

# BalancedRandomForestClassifier: 
<img width="268" alt="Screen Shot 2023-04-02 at 10 35 52 AM" src="https://user-images.githubusercontent.com/117120227/229369346-e0085178-5d78-4bb9-a517-f603c9967658.png">

<img width="561" alt="Screen Shot 2023-04-02 at 9 59 44 AM" src="https://user-images.githubusercontent.com/117120227/229367538-f87b48f7-a45a-419e-ac41-fdebc545ff62.png">
   
   We can see in this model that the balanced accuracy score is around 79%. The high_risk precision is still about 3%, with a 70% recall, making the F1 score still around 6%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100%, with recall of 87% and a F1 score of 93%.    
   
# EasyEnsembleClassifier: 
<img width="268" alt="Screen Shot 2023-04-02 at 10 38 55 AM" src="https://user-images.githubusercontent.com/117120227/229369474-727feabb-9900-4e3a-8acb-ea6051f7f343.png">

<img width="561" alt="Screen Shot 2023-04-02 at 10 00 22 AM" src="https://user-images.githubusercontent.com/117120227/229367565-1bf67037-1e0e-4263-b567-18213c6cb512.png">

   We can see in this model that the balanced accuracy score is around 93%. The high_risk precision is still about 9%, with a 92% recall, making the F1 score still around 16%. Comparing the high_risk to the low_risk population, low_risk recieved a  precision of almost 100%, with recall of 94% and a F1 score of 97%.   

# Summary:
   In summary, each of these machine learing models had relatively shown a weak recall in determining if credit risk was high. The Ensemble Classifiers appeared to be the most accurate model out of all them with higher accuracy, recall and F1  scores compared to the Over and Undersampling Models. However, each model does appear to be flawed with some having higher numbers of false positives and some having lower false positives. As a result, a recommendation would be to use the BalancedRandomClassifer since its results were in the middle. It did not have any extremely different results between the Over and Under sampling models and the ensemble classifiers.
