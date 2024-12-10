# Project-Disaster-Response-Pipeline

# Overview
This project is part of the Udacity Data Science Nanodegree Program. It focuses on building a machine learning pipeline to categorize disaster-related messages, enabling efficient responses during emergencies. The application processes messages and classifies them into categories, helping organizations like emergency response teams prioritize and act swiftly.

The project also includes an interactive web app where users can input new messages and view the classification results in real time. The app also displays visualizations of the dataset to provide insights into the distribution of categories.

## Repository Contents
The repository contains the following key components:

1. Data:

**disaster_messages.csv:** Contains messages collected from real-life disaster events.

**disaster_categories.csv:** Includes labels for each message indicating the relevant categories.

2. ETL Pipeline:

3. process_data.py: Extracts, transforms, and loads the data into a SQLite database. The script cleans the data by removing duplicates and unnecessary fields.

**Machine Learning Pipeline:**

1. train_classifier.py: Trains and evaluates a multi-output classification model using the cleaned dataset.
2. Web App:

app folder: Contains the Flask web app's front-end and back-end code.

Users can input messages for real-time classification and view various data visualizations.

## Jupyter Notebooks:

**Exploratory Data Analysis:** Initial analysis and visualization of the dataset.

**Supporting Files:**

1. README.md: Documentation of the project.
2. requirements.txt: List of Python dependencies.
   
## Project Workflow
### Data Preparation:

Load messages and categories datasets.
Clean and merge the datasets.
Store the cleaned data into a SQLite database.

### Model Building:

Build a machine learning pipeline to tokenize text, extract features, and classify messages.
Train and evaluate the model using accuracy, precision, recall, and F1-score metrics.
Save the trained model as a pickle file.

### Web Application:

Deploy the model in a Flask app.
Allow users to input new messages for classification.
Provide visualizations of message categories and dataset trends.

## Installation
### Prerequisites
**Make sure the following are installed:**
Python (>= 3.7)
Libraries: pandas, NumPy, scikit-learn, NLTK, SQLAlchemy, Flask, and Plotly.
Install the required dependencies:

**pip install -r requirements.txt**

Run the ETL pipeline:

**python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db**

Train the model:

**python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl**

Launch the web app:

**python app/run.py**


## Visualizations and Features
The web app includes:

**Message Classification:** Enter new messages and receive predicted categories.
**Interactive Charts:** Visualize the distribution of categories and data trends.
