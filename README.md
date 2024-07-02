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

3. Data Cleaning
   * Data cleaning is crucial as wrong data influence the model training process and further the result. With that, I conducted some analyses to check whether there were problems in the datasets given.

     The steps I did were:
       * Check missing values ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/6be62fcf-5bba-4c05-a0bb-4de00ddf0029)
         
       * Check "Age" column to see whether the data is correctly recorded ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/68a7f545-b1c6-427f-aff2-0e27572ba8b8)
         
       * Check whether columns "HasCrCard" as well as "IsActiveMember" contain wrong records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/f2e68e61-36b6-42f8-8dbb-667582eafce4)
    
       * Check whether columns "Geography" as well as "Gender" contains wrong or weird records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/a24bf7f5-a452-493d-a609-0e26f3ba05a8)
    
       * Check whether column "EstimatedSalary" contains wrong records ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/e873c6b2-9fb8-4fd1-b421-9be7b6091cdb)

5. Data Preprocessing
   * Data processing is always required for machine learning. What I did here were:
     1. Check the distribution of "Exited" data in train.csv, which in this case was unbalanced. This resulted in me deploying "oversample" in step 6. ![image](https://github.com/PingYenC/FIT-AID-Data-Scientist/assets/164700831/280614dc-4299-44bd-ac8b-eabde6b015de)
        
     2. 
7. Model Building
8. Model Evaluation
9. Result Storing
