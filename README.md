# Food-recognition-and-Calorie-Estimation-using-deep-learning

This project is a deep learning-based application for recognizing food items from images and estimating their calorie content. It uses Convolutional Neural Networks (CNNs) and is implemented using TensorFlow/Keras. The core idea is to classify a food image into one of 100 Japanese food categories and then estimate its calorie count based on predefined nutritional information.

Dataset Used: UECFOOD100
Link: UECFOOD100 on Kaggle
The UECFOOD100 dataset contains images from 100 Japanese food categories.
Each category has multiple images annotated with bounding boxes and food labels.
We assume each category corresponds to a standard calorie estimate.
The dataset is used both for training and evaluating the model.
Preprocessing includes image resizing, normalization, and (optionally) bounding box cropping.

Notebook Overview

📁 Notebook File: Foodrecognitionandcalroiesproject.ipynb
Key Sections:
1. Data Loading and Preparation
Images are read from the UECFOOD100 dataset directories.
Images are resized to a uniform shape (e.g., 224x224).
Labels are encoded as integers and used for classification.

2. Model Building
A CNN model (based on architectures like VGG or MobileNet) is constructed using Keras.
The final layer predicts the food class.
An optional mapping from class index to average calorie value is maintained.

3. Model Training
Categorical Crossentropy is used as the loss function.
The model is trained using the Adam optimizer.
Training accuracy and validation accuracy are monitored.

4. Model Evaluation
Accuracy metrics are reported.
The model is tested on a hold-out dataset or unseen food images.

5. Calorie Estimation
Once a food item is recognized, a predefined calorie mapping (e.g., dictionary of class → kcal) is used.
This part estimates the total calories in the given image.

6. Visualization and Inference
Sample predictions are shown with food class and estimated calories.
Charts for training vs validation accuracy/loss are plotted.
