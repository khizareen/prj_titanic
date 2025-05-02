# prj_titanic

# 🚢 Titanic Survival Prediction – End-to-End Machine Learning Pipeline with SQL Integration

## Project Overview :
This project presents an end-to-end machine learning solution for predicting Titanic passenger survival. The process starts with **loading data from a MySQL database using a SQL script**, followed by **data preprocessing**, **model training**, and **deployment through a Streamlit web application**.
The system is designed to show how machine learning can be effectively integrated with SQL for data storage and accessed through an intuitive UI.

## Objective : 
To build a machine learning model that predicts whether a passenger survived the Titanic disaster using key demographic and travel information.

## Tools and Technologies Used
- **Python** – for building the pipeline
- **MySQL** – to store the dataset in a relational format
- **SQLAlchemy** – for connecting Python with MySQL
- **Pandas, NumPy** – for data manipulation
- **Scikit-learn** – for machine learning model development
- **Matplotlib, Seaborn** – for data visualization
- **Streamlit** – for app deployment
- **Joblib** – for saving the trained model

## Dataset Information
The Titanic dataset is loaded into MySQL using a SQL script. The script creates a table named `titanic` with the following schema:

| Column Name   | Data Type       | Description |
|---------------|------------------|-------------|
| `PassengerId` | INT              | Unique identifier for each passenger |
| `Survived`    | INT              | Survival status (0 = No, 1 = Yes) |
| `Pclass`      | INT              | Passenger class (1 = First, 2 = Second, 3 = Third) |
| `Name`        | VARCHAR(255)     | Name of the passenger |
| `Sex`         | VARCHAR(10)      | Gender (male/female) |
| `Age`         | FLOAT            | Age of the passenger |
| `SibSp`       | INT              | Number of siblings or spouses aboard |
| `Parch`       | INT              | Number of parents or children aboard |
| `Ticket`      | VARCHAR(50)      | Ticket number |
| `Fare`        | FLOAT            | Fare paid for the ticket |
| `Cabin`       | VARCHAR(20)      | Cabin number (often missing) |
| `Embarked`    | VARCHAR(5)       | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

Some columns (like `Name`, `Ticket`, and `Cabin`) were dropped during preprocessing due to missing values or irrelevance for prediction.

## Project Workflow
1. **Data Loading**
   - Loaded Titanic data directly from a MySQL table using SQLAlchemy.
2. **Data Cleaning**
   - Removed irrelevant features and handled missing values.
   - Processed categorical variables using encoding techniques.
3. **Exploratory Data Analysis**
   - Analyzed survival rates across sex, class, age groups, etc.
   - Used plots to visualize important trends in the dataset.
4. **Feature Engineering**
   - Applied label encoding to categorical features.
   - Created new features such as age bins and family size.
5. **Model Training**
   - Used `RandomForestClassifier` for training the model.
   - Evaluated using accuracy, confusion matrix, and classification report.
6. **Model Saving**
   - Exported the trained model as a `.pkl` file using `joblib`.
7. **Model Deployment**
   - Created a user-friendly prediction app using **Streamlit**.
   - Users input values via the UI and receive survival predictions in real-time.

## Results
- Achieved strong predictive performance using Random Forest.
- Created an intuitive app to showcase the model.
- Demonstrated integration of SQL, machine learning, and web deployment.

## How to Run This Project
Clone the repository:
git clone (https://github.com/khizareen/prj_titanic).git
cd titanic
Install dependencies:
pip install -r requirements.txt
Run the Streamlit app:
streamlit run app.py

## Repository Structure
- `Titanic.sql`: SQL script to create and populate the Titanic table.
- `model.pkl`: Trained machine learning model saved to disk.
- `app.py`: Streamlit app for predictions.
- `requirements.txt`: Required Python dependencies.

## Deployment
The app is deployed on Streamlit Cloud.
Live URL: (https://prjtitanic-ubzqcbtstndevfs4sgervj.streamlit.app/)

## Author
[Khizareen Taj) GitHub: (https://github.com/khizareen))
