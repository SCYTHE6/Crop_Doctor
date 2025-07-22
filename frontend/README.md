# Crop Doctor: Plant Disease Detection Web App
# Crop Doctor is an AI-powered web application that helps in identifying diseases in crop leaves. Users can upload an image of a plant leaf, and the deep learning model at the backend will predict whether the leaf is healthy or affected by a specific disease. This tool can assist farmers in the early detection of crop diseases, potentially saving crops from significant damage.

# 🌱 Features

• Web Interface: A simple and intuitive web interface built with Flask for uploading leaf images.

• Deep Learning Model: Utilizes a Convolutional Neural Network (CNN) built with the Keras Functional API to classify images of plant leaves.

• Data Preprocessing: Uses scikit-learn to properly split the dataset into training and testing sets.

• Real-time Prediction: Provides instant predictions on the uploaded images.

• Scalable: The architecture separates the model training (in a Jupyter Notebook) from the web application deployment.

# 🛠️ Tech Stack

• Backend: Flask (Python)

• Frontend: HTML, CSS (using Jinja2 templates)

• Deep Learning: TensorFlow, Keras

• Data Science: NumPy, scikit-learn

• Image Processing: OpenCV, Pillow (PIL)

• Visualization: Matplotlib

# ⚙️ Setup and Installation

# 1 - Clone the repository:

# git clone https://github.com/SCYTHE6/Crop_Doctor.git
# cd Crop_Doctor

# 2 - Install dependencies:
It is highly recommended to use a virtual environment.

# pip install -r requirements.txt

(Ensure your requirements.txt file includes flask, tensorflow, numpy, scikit-learn, opencv-python, pillow, and matplotlib)

# 3 - Model Training (Optional):

• The repository contains the Crop_Doctor_Final.ipynb notebook, which has the code for training the CNN model.

• To train the model from scratch, you will need a dataset of plant leaf images, categorized into different disease classes.

• After training, save the model weights as an .h5 file and place it in the models/ directory. The application likely already includes a pre-trained model.

# 🚀 How to Run the Web App
The main application logic is in CropDoc.py.

# 1 - Ensure the trained model is in place:
Make sure a trained model file (e.g., model.h5) exists in the models/ directory.

# 2 - Run the Flask application:

# python CropDoc.py

# 3 - Access the application:
Open your web browser and navigate to http://127.0.0.1:5000 (or the address shown in your terminal).

# 4 - Use the App:

• You will see a page with an "Upload" button.

• Click the button and select an image of a plant leaf from your computer.

• The application will process the image and display the model's prediction for the plant's health status.

# 🧠 Model Information

# • Architecture: The model is a Convolutional Neural Network (CNN) built using the Keras Functional API, which allows for more flexible model architectures. It consists of:

• Conv2D layers for feature extraction.

• MaxPool2D layers for down-sampling.

• A Flatten layer to prepare the features for classification.

• Dense layers for the final classification.

• Dataset: The model was trained on a dataset of images of plant leaves. The Crop_Doctor_Final.ipynb notebook contains details about the dataset structure, preprocessing steps, and the use of train_test_split for creating a robust validation set.

• Output: The model outputs a prediction, which is the name of the disease or "Healthy".

# 📁 Project Structure
.
├── CropDoc.py              # Main Flask application file
├── Crop_Doctor_Final.ipynb # Jupyter Notebook for model training
├── models/
│   └── model.h5            # Pre-trained model file
├── static/                 # CSS, JS, and other static assets
│   └── css/
├── templates/              # HTML templates for the web pages
│   └── index.html
├── test/                   # Sample images for testing
└── requirements.txt        # Python dependencies
