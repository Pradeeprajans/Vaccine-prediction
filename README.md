# H1N1 & Seasonal Flu Vaccination Prediction

This is a **web-based application** built using **Flask**, which predicts the likelihood of an individual getting the **H1N1** or **Seasonal Flu** vaccine based on various personal, behavioral, and demographic factors. It relies on machine learning models trained on vaccination-related data to make predictions. The app collects user input through a web form and uses pre-trained models to predict the likelihood of vaccination.

## Features

- **H1N1 Vaccine Prediction**: This predicts if a person will take the H1N1 vaccine based on his answers regarding how concerned he is about H1N1, his health behaviors, what the doctor recommended, and much more.
  
- **Seasonal Flu Vaccine Prediction**: The same, predict how likely it is for someone to get the seasonal flu vaccine based on his responses.

- **Interactive Web Interface**: The user interacts with a clean, intuitive form where they can select options related to their health, knowledge, behavior, and social interactions.

- **Real-Time Predictions**: Once the user submits the form, the app processes the data through a trained machine learning model and returns the prediction about the likelihood of receiving either the H1N1 or Seasonal Flu vaccine.

## Project Structure

- **app.py**: This is the main Flask application file that runs the web server and handles the routing of user inputs. It includes endpoints for displaying the form, processing form submissions, and serving the prediction results.
  
- **h1n1_gradient_boosting_model.pkl**: A serialized machine learning model for predicting H1N1 vaccine uptake.
  
- **seasonal_gradient_boosting_model.pkl**: A serialized machine learning model for predicting Seasonal Flu vaccine uptake.

- **templates/**
- **index.html**: The HTML template for the main form in which users input their details to be predicted.
  - **result_h1n1.html**: Shows the result of the H1N1 vaccine prediction.
  - **result_seasonal.html**: Shows the result of the Seasonal Flu vaccine prediction.

- **static/**
  - **style.css**: CSS file for styling the web pages.

## How the Trained Model Files are Deployed

The machine learning models for both **H1N1 vaccine prediction** and **Seasonal Flu vaccine prediction** are saved as **Pickle (.pkl) files**. These models are loaded into the **Flask backend** when the user submits the form.

### Model Deployment Workflow:
1. **User Submission**: The user submits their responses through a form.
2. **Data Preprocessing**: The Flask application processes the form data to match the format expected by the model.
3. **Model Prediction**:
- The processed data is fed into the pre-trained models.
  - The model predicts based on the input features.
4. **Result Display**: The Flask app then returns the prediction result to the user through the `result_h1n1.html` or `result_seasonal.html` page.

The models are loaded at the start of the app and are used every time the user submits the form.

## How to Run the Web Application

To run the Flask application locally, follow these instructions:

### 1. Clone the Repository
Clone this repository to your local machine:
```bash 
git clone https://github.com/your-username/vaccine-prediction.git 
cd vaccine-prediction 
```

# 2. Install Dependencies
Make sure that Python is installed. Then run this command to install all of the dependencies:
 
### 2. Install Dependencies

Make sure you have Python installed. Then, run this command to install all of the dependencies:

```bash
pip install -r requirements.txt 
```

### 3. Add Model Files

Make sure that the trained model files, `h1n1_gradient_boosting_model.pkl` and `seasonal_gradient_boosting_model.pkl`, are in the root directory of the project. They are needed to make predictions.

These are the pre-trained machine learning models used to predict the probability of H1N1 and Seasonal Flu vaccination based on the form data submitted by the user. Without these model files, the application will not work properly.

### 4. Run the Flask Application

To start the Flask development server, run the following command in your terminal:

```bash
python app.py
```

### 5. Access the Application

After running the Flask application, open your browser and navigate to `http://127.0.0.1:5000`. You should see a form asking for your details. 

After filling out the form, you can click either the **"Predict H1N1 Vaccine"** or **"Predict Seasonal Vaccine"** button to get the vaccination prediction result based on the data you provided.


Conclusion

This project is a practical application for predicting vaccination likelihood based on personal, behavioral, and demographic factors. Using machine learning models that are deployed with **Flask**, users can receive predictions about the **H1N1** and **Seasonal Flu** vaccines in real-time.

The app is designed to be easily deployable, and you can run it locally or deploy it on cloud platforms for broader access.
