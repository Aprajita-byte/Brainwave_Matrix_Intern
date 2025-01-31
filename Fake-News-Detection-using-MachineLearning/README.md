# Fake News Detection using Machine Learning

## Table of Contents
- [Introduction](#introduction)
- [Problem Definition](#problem-definition)
- [Project Structure](#project-structure)
- [Datasets](#datasets)
- [Model Name](#model-name)
- [Images](#images)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)

## Introduction
This repository hosts an extensive project focused on fake news detection through machine learning and natural language processing methods. It encompasses data analysis, model training, and a web application for real-time detection. The machine learning model is built to determine whether news articles are genuine or fabricated based on their content.

## Problem Definition
Our goal is to create a machine learning program that identifies news sources likely to produce fake news. The model will evaluate multiple articles from each source to determine if it consistently disseminates false information. Once a source is flagged as a producer of fake news, we can confidently predict that future articles from that source are also likely to be fake. By concentrating on sources, we can tolerate a higher rate of individual article misclassification, as each source provides multiple data points for analysis.

The project's intended application is to assign visibility weights in social media platforms. By leveraging the weights generated by this model, social networks can reduce the visibility of stories that are highly likely to be fake news.

## Project Structure
The repository is organized into the following directories and files:
- **Images**: Contains important project images, such as block diagrams, classification reports, confusion matrices, and screenshots.
- **dataset**: Includes the dataset, consisting of train and test data from Kaggle, which is used to train and test the model.
- **static**: Houses static assets for the web application, including CSS, JavaScript, etc.
- **templates**: Includes HTML templates for the web application, such as `Landingpage.html` and `prediction page.html`.
- **Fake_News_Detector-PA.ipynb**: Jupyter Notebook file for data analysis and model training.
- **app.py**: Flask web application for real-time fake news detection.
- **model.pkl**: Pre-trained machine learning model for fake news detection.
- **vector.pkl**: Pre-trained vectorizer for text data.

## Datasets 
### train.csv
A full training dataset with the following attributes:
- `id`: unique id for a news article
- `title`: the title of a news article
- `author`: author of the news article
- `text`: the text of the article; could be incomplete
- `label`: a label that marks the article as potentially unreliable
  - `1`: unreliable
  - `0`: reliable

### test.csv
A testing training dataset with all the same attributes as `train.csv` without the label.

## Model Name
The machine learning model used for fake news detection in this project is the **Passive Aggressive Classifier**.

### Model Description
The Passive Aggressive Classifier (PAC) is a type of online learning algorithm for binary classification tasks. It is well-suited for applications like fake news detection. The PAC algorithm updates its model continuously as new data arrives, making it efficient for real-time classification.

### Model Accuracy
The Passive Aggressive Classifier achieved an impressive accuracy of **96%** during evaluation. This high accuracy indicates its effectiveness in classifying news articles as reliable or unreliable.

The model is pre-trained and available as `model.pkl` in this repository, allowing you to use it for making predictions.

Feel free to explore the Jupyter Notebook (`Fake_News_Detector-PA.ipynb`) for more details about the model's training and performance.

## Images
This section provides visuals and diagrams used in the project:
- Block Diagram
![Block Diagram](Images/BlockDiagram.jpg)

- Process Flow Diagram
![Process Flow Diagram](Images/Processflow.jpg)

- Confusion Matrix
![Confusion Matrix](Images/ConfusionMatrix.jpg)

## Prerequisites
Before you begin, ensure you have met the following requirements:
- Python 3.7 or higher
- Install all dependencies from the requirements.txt file.

## Getting Started
To get started with this project, follow these steps:
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Aprajita-byte/Brainwave_Matrix_Intern
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv my_env
   ```

3. Activate the virtual environment:
   ```bash
   # On Windows
   .\my_env\Scripts\Activate.ps1
   # On macOS and Linux
   source my_env/bin/activate
   ```

4. Install project dependencies:
   ```bash
   pip install -r requirements.txt
   ```

5. Run the web application:
   ```bash
   python app.py
   ```

Access the application in your web browser by navigating to `http://localhost:5000`.

---

**Author**
- Aprajita Sharma (https://github.com/Aprajita-byte)


---
