# Plant Leaf Disease Prediction System

This project is a deep learning-based application to predict diseases in tomato plant leaves. The system uses a Convolutional Neural Network (CNN) to classify leaf images into different categories of diseases. The project includes both the training of the model and a front-end application for users to upload images and receive predictions.

## Importance of the Project

Plant diseases can significantly impact agricultural productivity and quality. Early and accurate detection of plant diseases is crucial for effective management and control, which can lead to improved crop yields and reduced economic losses. This project aims to provide a reliable and automated solution for identifying various diseases in tomato plants, assisting farmers and agricultural professionals in maintaining healthy crops.

## Project Structure

### Training Code

The training code is written in Python using TensorFlow and Keras. The CNN model is built with several convolutional and pooling layers, followed by dense layers for classification. The model is trained on a dataset of tomato leaf images with various diseases.

- **Convolutional Neural Network (CNN):**
  - **Input Shape:** (128, 128, 3)
  - **Layers:**
    - Conv2D, MaxPooling2D
    - Flatten
    - Dense layers

- **Data Augmentation:**
  - `ImageDataGenerator` is used for data augmentation to improve the model's generalization.

- **Training:**
  - The model is compiled with Adam optimizer and categorical cross-entropy loss.
  - It is trained for 50 epochs with a batch size of 6.

### Front-End Application

The front-end is built using Flask, a lightweight web framework for Python. It allows users to upload an image of a tomato leaf, which is then processed and classified by the trained model. The application returns the predicted disease and displays an appropriate HTML page with information about the disease.

- **Flask Application:**
  - **`/` route:** Renders the home page where users can upload an image.
  - **`/predict` route:** Handles the image upload, calls the prediction function, and renders the result page.

- **Prediction Function:**
  - Loads and preprocesses the image.
  - Uses the trained model to predict the disease.
  - Maps the prediction to the corresponding disease and HTML page.

## Dataset and Model Download

- [Download Dataset](https://drive.google.com/drive/folders/1ctFfEFq03H7sqQiBQxNlbYpi-g1kqcR2?usp=drive_link)  
- [Download Saved Model](https://drive.google.com/drive/folders/1ctFfEFq03H7sqQiBQxNlbYpi-g1kqcR2?usp=drive_link) 
