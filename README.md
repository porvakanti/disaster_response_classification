# Disaster Response Pipeline Project

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### Background:
Following a disaster, different types of disaster response organizations take care of different parts of the disasters and observe messages to understand the needs of the situation. They have the least capacity to filter out messages during a large disaster, so predictive modeling can help classify different messages more efficiently.

In this project, I built an ETL pipeline that cleaned messages using regex and NLTK. The text data was trained on a multioutput classifier model using random forest. The final deliverable is Flask app that classifies input messages and shows visualizations of key statistics of the dataset.

The random forest classifier model scored 74% accuracy, 98% precision, 78% recall, and 87% F-1 score after tuning the parameters using GridSearchCV.

### Files:
1. process_data.py : ETL script to clean data into proper format by splitting up categories and making new columns for each as target variables.
2. train_classifier.py : Script to tokenize messages from clean data and create new columns through feature engineering. The data with new features are trained with a ML pipeline and pickled.
3. run.py : Main file to run Flask app that classifies messages based on the model and shows data visualizations.

### Screenshots:

![alt text](https://github.com/porvakanti/disaster_response_classification/blob/master/images/1.PNG)

![alt text](https://github.com/porvakanti/disaster_response_classification/blob/master/images/2.PNG)
