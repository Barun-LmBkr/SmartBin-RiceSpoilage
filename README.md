# SmartBin: ML Classifier for Spoilage Detection in Stored Grains

**SmartBin** is a machine learning-powered system designed to predict the spoilage status of stored rice grains based on environmental factors like temperature, humidity, grain moisture, and dew point. This project aims to help optimize grain storage by providing real-time predictions to minimize spoilage and loss.

## Features

- **Data Preprocessing**: Handling missing values, encoding labels, and feature scaling.
- **Model Training**: Using XGBoost Classifier to predict spoilage classes (`Safe`, `Risky`, `Spoiled`).
- **Hyperparameter Tuning**: Optimizing the model using Optuna for better performance.
- **Prediction**: Real-time spoilage prediction via a user-friendly Streamlit interface.
- **Model Deployment**: A simple Streamlit app that allows users to input real-time data and get spoilage predictions.

## Requirements

To run the project, you need to have the following Python packages installed:

- pandas
- numpy
- scikit-learn
- xgboost
- joblib
- optuna
- streamlit
- seaborn
- matplotlib

You can install them using the following command:

```bash
pip install -r requirements.txt
Files in the Repository
train_model.py: Script to train the model using XGBoost, save the model as a .pkl file.

preprocessing.py: Contains functions for loading and preprocessing the data, including missing value handling and feature scaling.

hyperparameter_tuning.py: Implements Optuna-based hyperparameter tuning for the XGBoost model.

predict.py: Includes the prediction logic to load the trained model and make predictions on input data.

app.py: Streamlit-based application for real-time predictions of spoilage status.

smartbin_rice_storage_data_enhanced.csv: Sample dataset used to train and evaluate the model.

requirements.txt: List of required dependencies to run the project.

How to Run the App
Train the Model (if you haven't already):

First, run the following command to train the model and save it:

bash
Copy
Edit
python train_model.py
Run the Streamlit App:

After the model is trained and saved as smartbin_model.pkl, you can start the Streamlit app to make predictions:

bash
Copy
Edit
streamlit run app.py
This will open a browser window with the interface where you can input real-time data for prediction.

How to Use
Input the following parameters in the app:

Temperature: The temperature of the storage environment.

Humidity: The relative humidity of the storage environment.

Grain Moisture: The moisture content in the rice grains.

Dew Point: The dew point of the storage area.

The app will provide a spoilage classification based on the input values:

Safe: The grains are in good condition.

Risky: The grains might be at risk of spoilage.

Spoiled: The grains are spoiled and should not be consumed.

Limitations
While SmartBin offers valuable insights into spoilage detection, there are a few limitations:

Limited Data: The model is trained on a specific dataset that may not generalize well to other types of grains or storage environments. More diverse datasets would improve the model's robustness.

Environmental Factors: The model uses only four features (Temperature, Humidity, Grain Moisture, and Dew Point). Other factors, like air circulation, pest presence, and storage conditions, could significantly impact spoilage but are not considered here.

Model Interpretability: While XGBoost provides good performance, the model's "black-box" nature can make it harder to interpret specific predictions in certain cases.

Real-time Data: The app requires manual input of data. In a real-world scenario, the system could benefit from sensors that automatically feed real-time environmental data into the system.

Future Advancements
There are several potential directions for improving and expanding this project:

Integration of IoT Sensors: Incorporating real-time data from IoT sensors in storage areas to automate data collection for more accurate and timely predictions.

Broader Dataset: Expanding the dataset to include more grains, environmental factors, and spoilage conditions, which would enhance the model's ability to generalize across various types of grains and conditions.

Explainability Tools: Implementing explainability tools like SHAP or LIME to make the model’s predictions more interpretable, helping users understand why a certain prediction (e.g., "Risky") was made.

Mobile App Development: Developing a mobile app to enable on-the-go spoilage prediction for farmers and grain handlers, providing easier access to the system.

Advanced Models: Exploring deep learning or other advanced machine learning techniques to improve predictive accuracy, especially in more complex storage environments.

Contributing
Feel free to contribute to this project. You can fork this repository, make changes, and create a pull request. Please make sure to follow the repository's guidelines for contributions.

License
This project is open-source and available under the MIT License. See the LICENSE file for more details.

Author
Barun
Email: barun.vsaha@gmail.com
GitHub: Barun-Lmbkr