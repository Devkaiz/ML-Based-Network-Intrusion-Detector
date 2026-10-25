# ML-Based Network Intrusion Detector

## Project Overview
This project uses a Machine Learning model to classify network traffic as **BENIGN** or **DDoS (Distributed Denial of Service)** based on network-flow features. A Random Forest classifier is trained using labelled traffic data from the CIC-IDS2017 dataset.

## Problem Statement
DDoS attacks can overwhelm online services with excessive traffic and affect their availability. This project explores how machine learning can help distinguish benign traffic from traffic associated with DDoS attacks.

## Objectives
- Load and preprocess network traffic data.
- Train a Random Forest classification model.
- Evaluate the model using accuracy, precision, recall, F1-score, and a confusion matrix.
- Examine important features used by the model.
- Demonstrate predictions on sample network-flow records.

## Dataset
- **Name:** CIC-IDS2017
- **Official dataset page:** https://www.unb.ca/cic/datasets/ids-2017.html
- **Selected data:** Friday Afternoon DDoS traffic CSV
- **Target classes:** BENIGN and DDoS

The dataset contains labelled network-flow records for research and machine-learning experiments.

## Technologies Used
- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Joblib

## Methodology
1. Load and inspect the dataset.
2. Clean missing, infinite, and duplicate records.
3. Separate input features from target labels.
4. Split the data into training and testing sets.
5. Train a Random Forest classifier.
6. Evaluate classification performance.
7. Visualize feature importance and test sample predictions.
8. Save and reload the trained model.

## Setup and Run Instructions

### 1. Open the notebook
Open the project notebook in Google Colab.

### 2. Install dependencies
Run the following command in a notebook cell if the required packages are not already installed:

```python
!pip install -r requirements.txt
```

Upload `requirements.txt` to the Colab session first, or install the packages directly:

```python
!pip install pandas numpy scikit-learn matplotlib joblib
```

### 3. Load the dataset
Download the required CSV file from the official CIC-IDS2017 dataset page and upload it to Google Colab. Update the file path in the notebook if necessary.

### 4. Run the notebook
Run the cells in order, from dataset inspection and preprocessing through model training, evaluation, and prediction.

## Model and Results
The project uses a Random Forest classifier for binary classification.

Evaluation metrics include:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

The notebook contains the evaluation outputs from the experiment. Report the results corresponding to the dataset and model run used for the final submission.

## Limitations
- The model classifies only BENIGN and DDoS traffic in this experiment.
- The model uses previously collected, labelled network-flow data.
- It does not currently capture or classify live network traffic.
- Results on this dataset do not guarantee the same performance on unseen networks.

## Future Improvements
- Test the model on additional attack categories.
- Evaluate performance on independent datasets.
- Explore live network traffic integration.
- Develop a simple interface to display predictions.

## Disclaimer
This project is intended for educational and research purposes. It demonstrates machine-learning-based network traffic classification and is not a replacement for a production intrusion detection system.
