# 🔬 Techniques Used in the Code  

The **3oshbetna Backend & Model Training** project incorporates multiple machine learning and software engineering techniques to ensure efficient image processing, classification, and deployment.  

## 🖼️ Image Preprocessing & Augmentation  
- **Resizing & Normalization**:  
  - Images are resized to **224x224 pixels** for compatibility with **ResNet-50**.  
  - Normalization is applied using `tf.keras.applications.resnet50.preprocess_input` to scale pixel values.  
- **Batch Processing**:  
  - Input images are converted into **NumPy arrays** and expanded to match the model's input shape.  

## 🤖 Deep Learning Model (ResNet-50)  
- **Transfer Learning**:  
  - A **pre-trained ResNet-50 model** is used, fine-tuned on a custom dataset of Jordanian plant species.  
- **Multi-Class Classification**:  
  - The model outputs probabilities for each plant class.  
- **Top-N Prediction Ranking**:  
  - The API returns the **top-3 most likely species** along with confidence scores.  

## 🌐 Flask API for Model Deployment  
- **RESTful API Architecture**:  
  - Built with **Flask** to provide an endpoint (`/predict`) for image classification.  
- **CORS Handling**:  
  - `flask_cors` enables cross-origin requests, allowing communication between the backend and the Flutter frontend.  
- **Error Handling & Logging**:  
  - Implements exception handling for **model loading, prediction failures, and missing files**.  
