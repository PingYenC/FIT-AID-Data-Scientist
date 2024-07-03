# FIT-AID-Data-Scientist
This is an interview assignment for the role of FIT AID: Data Scientist.

# File Descriptions
* The original data given by FIT is the files "test.csv" and "train.csv", they were used to build the predictive model.
* Task 1 questions were answered in the file "Task_1_Answer.md".
* Task 2 tasks were completed and recorded in the file "Task_2_Code_File.ipynb".
* Task 2 output was stored in the file "Task_2_CSV_Predictions_Performance.csv".

# Assignment Description
The assignment is about answering some general interview questions (Task 1) and completing a coding task (Task 2) of building predictive models.

Task 1 includes general questions:
1. What is your preferred language when building predictive models and why?
2. Provide an example of when you used SQL to extract data.
3. Give an example of a situation where you disagreed upon an idea or solution design with a co-worker.  How did you handle the case?
4. What are your greatest strengths and weaknesses and how will these affect your performance here?

Task 2 objectives:

Given the dataset, train.csv (the training dataset); Exited is the binary target and test.csv (the test dataset);
your objective is to predict the probability of Exited and write a Python script (main.py) that when run (e.g. python main.py) will output:
1. A CSV file containing "Predicted Exited from test.csv" and "Evaluation of the predictive ability of the model.(e.g. F1 Score, Confusion Matrix…etc)"
2. Plots that can help us visualize the classification data and the prediction curves.

# Task 1 Answer
Please refer to the file "Task_1_Answer.md".

# Task 2 Explanation
1. Data Loading
   * Since I did the work in the Google Colab platform, I created a function that could load the data from my Google Drive file, which allowed me to run to codes without uploading the files each time.
     ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/3de72e74-0b1b-4c03-9aa6-b86222814c77)

2. Data Cleaning
   * Data cleaning is crucial as wrong data influence the model training process and further the result. With that, I conducted some analyses to check whether there were problems in the datasets given.

     The steps I did were:
       * Check missing values ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/6be62fcf-5bba-4c05-a0bb-4de00ddf0029)
         
       * Check "Age" column to see whether the data is correctly recorded ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/68a7f545-b1c6-427f-aff2-0e27572ba8b8)
         
       * Check whether columns "HasCrCard" as well as "IsActiveMember" contain wrong records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/f2e68e61-36b6-42f8-8dbb-667582eafce4)
    
       * Check whether columns "Geography" as well as "Gender" contains wrong or weird records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/a24bf7f5-a452-493d-a609-0e26f3ba05a8)
    
       * Check whether column "EstimatedSalary" contains wrong records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/e873c6b2-9fb8-4fd1-b421-9be7b6091cdb)

3. Data Preprocessing
   * Data processing is always required for machine learning. What I did here were:
     1. Check the distribution of "Exited" data in train.csv, which in this case was unbalanced. This resulted in me deploying "oversample" in step f. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/280614dc-4299-44bd-ac8b-eabde6b015de)
        
     2. Split the data into input (X-axis) and output (Y-axis) for the model. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/8c7b176a-a2d3-4b33-bf63-819954dabec0)
    
     3. Encode the data to make categorical values into numerical, which is essential for some machine learning methods. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/40ff991f-c056-4a93-9a05-a55a6cbbef05)
    
     4. Make the values in columns "Balance" and "EstimatedSalary" to values within a range of 0 and 1 due to their wide distributions. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/89d555af-ba0a-4807-a95a-146f21c1ea8d)
    
     5. Split the data into training and validation data for building and evaluating the models' training. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/9e6a045c-d520-4999-86ee-890eb957a21d)
    
     6. Use "oversample" technique to balance the training data. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/470b28fc-c9b1-43bb-939a-91ebd025abbf)

4. Model Building
   * After completing the data preprocessing, we can use the data to train models. I used a total of 4 different machine learning (deep learning) methods to build the predictive models.
     - KNN (K-Nearest Neighbors) algorithm:
    
       KNN is a popular and easily understandable method used for classification-prediction tasks, which was the reason I chose it for try and error. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/6a66ecf2-73cf-4b97-82af-a5809b4a4495)
    
     - Logistic Regression algorithm:
    
       Logistic Regression is a popular and easily understandable method for binary classification-prediction tasks. It is known for its power to explain logistic-regression distributed data. I used this method to test whether the data was distributed that way. For this method, I implemented grid-search on l1 or l2 penalty to avoid overfitting. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/0b355d13-3320-4433-b4df-957ab1a85862)

    
     - XGBoost (Extreme Gradient Boosting) algorithm:

       XGBoost is a gradient-boosted decision tree machine learning method and a famous and powerful approach to solving various types of tasks. It is capable of combining the predictions of multiple decision trees for a stronger prediction. That's the reason I chose it. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/36f9cd22-d1e3-4b69-964f-eaf4d09935d1) ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/263c6725-1119-4063-a9bb-9de19536ea71)

     - Deep Learning:
    
       Deep learning allows the machine to find patterns from data on its own. This method was chosen due to its capability to identify hidden relationships among the dataset without extensive work (please refer the coding to the "Task_2_Code_File.ipynb"). ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/962c98cb-4fa9-4355-9ee6-f10c4144340f)
 ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/59bac517-2318-453b-bcfa-8b4f1d8c67a7)


During the model-building process, I used grid-search on machine learning (KNN, Logistic Regression, and XGBoost) to find the best parameters for each algorithm, and provided deep learning method with a setting of "1 input layer, 2 hidden layers (ReLu), 1 output layer (sigmoid)" as it was the most efficient setting I found after several sessions. The detailed setting for deep learning is as below: ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/cf17e5a2-826d-4238-b844-fba38fd7b72a)

       
5. Model Evaluation
   * By comparing the validation performance for each method, I found out that the deep learning method offered the best result, with an 85% overall prediction accuracy and a 66% f1 score.
     ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/e4a3cda7-d08e-4109-a3a2-8f740374f65d)


   * Looking at the confusion matrix for each method, I concluded that while XGBoost performed better in forecasting 1 than Deep learning did, it performed worse in forecasting 0. Hence, deep learning was the most powerful method of making robust predictions. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/e1e4e116-7d93-4af1-ab08-98e7421b5329)

  
   * The below graph of the Precision-Recall curve proves my conclusion by showing that the model trained by the deep learning method maintained a high recall rate when the precision rate was high. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/9114087e-435b-4599-9420-b591a84f47f4)


6. Result Storing and Conclusion
   * I used the four trained models to make predictions on the testing data, which is the file "test.csv" and stored the predictions with the original data in a CSV file. You can refer to the file "Task_2_CSV_Predictions_Performance". It contains each model's performance as well.
   * Visualizing the predictions on the testing data, I found out that different models had slightly different predictions, making the distribution of the predictions different from each other. This was caused by the difference in each model's capabilities. Since I concluded that deep learning was the best model out of the four we had, I suggest focusing on and trusting the predictions from the deep learning model. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/57ce2357-5b8b-4b5c-81be-b63a6944c358)


