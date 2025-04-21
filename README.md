# Smart-Health-monitoring-system

## Overview
The **Smart Health Monitoring System** is a machine learning-based application designed to analyze patient health data and predict health conditions, with a focus on menstrual cycle prediction. It processes various health metrics such as heart rate, blood pressure, SpO2, stress levels, and more, using multiple machine learning algorithms (Naive Bayes, Decision Tree, Logistic Regression, and Support Vector Machine). The system also provides a web-based interface for real-time health metric input and analysis, built with **React** and **Tailwind CSS**.  
This project aims to assist healthcare professionals by providing predictive insights and health alerts based on patient data, enabling early intervention and personalized care.

## Features

- **Data Preprocessing**: Cleans and processes patient health data, including splitting blood pressure into systolic and diastolic components, and enforces gender-based menstrual cycle constraints.
- **Data Visualization**: Generates bar charts, histograms, countplots, KDE plots and heatmaps to visualize health metrics and correlations.
- **Machine Learning Models**:
    - Naive Bayes
    - Decision Tree
    - Logistic Regression
    - Support Vector Machine
- **Health Analysis**: Evaluates patient data to detect risks like tachycardia, hypertension, hypoxemia, chronic stress, and stress-related issues.
- **Menstrual Cycle Prediction**: Uses logistic regression to predict whether a patient is in their menstrual cycle and Ensures male patients cannot have a menstrual cycle, with appropriate UI and prediction adjustments.
- **Web Interface**: Allows users to input health metrics and view real-time analysis, predictions and health alerts.
- **Responsive Design**: Styled with **Tailwind CSS** for a modern, user-friendly experience.

## Dataset
The dataset (`patient_health_data.csv`) contains the following health metrics for multiple patients:
- **Patient ID**
- **Heart Rate (bpm)**
- **SpO2 (%)**
- **Sleep Duration (hrs)**, **Light Sleep (hrs)**, **Deep Sleep (hrs)**, **REM Sleep (hrs)**
- **Steps Count**, **Calories Burned**, **Distance Walked (km)**
- **Stress Level (1-10)**
- **Respiratory Rate (breaths/min)**
- **ECG (Normal=1, Irregular=0)**
- **Blood Pressure (Sys/Dia)**
- **Skin Temperature (°C)**
- **Menstrual Cycle (Yes=1, No=0)**
- **Fall Detected (Yes=1, No=0)**
- **Water Intake (litres)**
- - **Gender (Female=1, Male=0)**

The dataset is preprocessed to split blood pressure into systolic and diastolic columns and handle missing values.

## Installation

1. **Clone the Repository**:
    ```bash
    git clone <repository-url>
    cd smart-health-monitoring-system
    ```

2. **Install Python Dependencies**:
   Ensure Python 3.8+ is installed, then install the required packages:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

3. **Run the Python Script**:
   Execute the analysis script:
    ```bash
    python analyze.py
    ```

4. **Serve the Web Interface**:
   Open `index.html` in a browser. No additional server is required as it uses CDN-hosted libraries (React, Tailwind CSS, Babel).

## Usage

### Python Analysis:
- Run `analyze.py` to preprocess the dataset, visualize data, train machine learning models, and evaluate their performance.
- The script outputs accuracy scores, confusion matrices, and a comparison plot of model accuracies.
- It also performs a health analysis for a sample patient and predicts their menstrual cycle status.

### Web Interface:
- Open `index.html` in a browser.
- Enter health metrics (heart rate, systolic, diastolic, SpO2, steps count, stress level, ECG).
- View real-time health analysis and menstrual cycle predictions.
> **Note**: The web interface uses a simplified logistic regression model for demonstration purposes.

## Project Structure

## Results

### Model Performance:
- **Naive Bayes**: [Accuracy printed in output]
- **Decision Tree**: [Accuracy printed in output]
- **Logistic Regression**: [Accuracy printed in output]
- **Support Vector Machine**: [Accuracy printed in output]

### Health Analysis:
- Provides actionable insights, such as detecting tachycardia, hypertension, or stress-related risks.

### Web Interface:
- Offers an intuitive way to input data and view predictions, with alerts for critical health conditions.

## Limitations
- The dataset is relatively small, which may limit model generalization.
- The web interface uses a simplified logistic regression model, not the full trained model from `analyze.py`.
- The system is a prototype and should not replace professional medical diagnosis.

## Future Improvements
- Expand the dataset with more patient records and features and Integrate actual gender data into patient_health_data.csv .
- Integrate the full machine learning models into the web interface using a backend (e.g., Flask).
- Add real-time data streaming from wearable devices.
- Enhance the UI with interactive charts using Recharts or similar libraries.

## Contact
For questions or contributions, please contact nancydwivedi1234@gmail.com or open an issue on the repository.
