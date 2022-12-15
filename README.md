PROJECT/PURPOSE
UDACITY PROJECT DATA ENGINEERING "Disaster Response Pipelines"

TITLE
Machine learning pipeline to categorize disaster messages and transfer the messages to an appropriate disaster relief agency.

PROJECT MOTIVATION
As part of my Udacity Data scientist training, this project allows implementing a machine learning script.

DESCRIPTION:
The Web app, based on python scripts and messages databases, allows loading files of messages, clean the messages before building a machine learning.
Once trained, the model allows categorizing new messages for a further transfer to the appropriate relief agency (this last is not include into the app).

PROCESSING AND ANALYSIS:
Processing is divided in three parts:
- Extract, Transform, and Load (ETL) consisting in loading messages and categories csv sheets of messages and categories, merge them before transformation into a python dataframe.
  Next, the dataframe is cleaned before being converted into a SQLite database. During this process, categories field is split as dummy boolean data.
- Machine Learning (ML) Pipeline, based on GridSearchCV, processes every messages to extract main words (tokenization) and classify these messages for the fit and train the model.
  Based on this trained model, we're able to give the accuracy of the model and predict classification of every new messages.
- The app is available through a web interface that allows entering a new message; then the user request a classification into appropriate categories.
  A vizualisation allows getting an overiew of the distribution of the messages along these categories.  
  
VERSION:
ID: 1.1.0
This version is the initial version

PUBLIC RELEASE  
You can find the published released here:
TBD

ENVIRONNEMENT
ETL and ML are coded in python 3 under the Jupyter Notebook server in version 5.7.0.
Jupyter Notebook relies on Python 3.6.3 packaged by conda-forge.
For further details, refer to requirements.txt


REPOSITORY'S FILE
- File "README.md"
- Folder "Jupyter_Notebook_dashboard" with files for running on Jupyter Notebook environment.
  This folder contains: "messages.csv", "categories.csv", "DisasterResponse.db", "ETL Pipeline Preparation.ipynb" and "ML Pipeline Preparation.ipynb"
- Folder "Web_app_workspace_IDE" with files for running the Web App.
  This folder contains: "README.md" ; folder "app" with "run.py" and folder "templates" (with "go.html" and "master.html") ; folder "data" with "disaster_categories.csv", "disaster_messages.csv", "DisasterResponse.db", "process_data.py" ; folder "models" with "classifier.pkl" and "train_classifier.py"

DATA SOURCE
Data are provided by https://learn.udacity.com/

ACKNOLEDGMENTS:
Data set credit: https://appen.com/

LEGAL / LICENSE:
Refer to Udacity and APPEN data access rights
