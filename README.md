# Ambatik Machine Learning Documentation
Welcome to the comprehensive documentation for our machine learning models! 

## Libraries

1. **Keras:** An user-friendly neural network framework with a high-level interface for model development and training that is constructed on top of TensorFlow.

2. **NumPy:** An vital Python library for scientific computing that handles matrices, arrays, and mathematical operations.

3. **TensorFlow:** A Google-developed open-source machine learning framework for creating and refining machine learning models.

4. **Matplotlib:** A complete Python visualization toolkit.

## Dataset

The dataset used in this project comprises a collection of **1,130 images** distributed across 15 distinct classes representing various traditional Indonesian batik:

**Cendrawasih**
**Geblek Renteng**
**Insang**
**Kawung**
**Lasem**
**Mega Mendung**
**Nitik**
**Parang**
**Poleng**
**Pring Sedapur**
**Sekar Jagad**
**Simbut**
**Sogan**
**Tambal**
**Truntum**

## Model Architecture

This project employs transfer learning with the EfficientNetV2M architecture:

**Base Model:** Utilizes a pre-trained EfficientNetV2M model with ImageNet weights.

**Freezing Layers:** Some layers are frozen to retain pre-learned features and prevent retraining.

**Customization:** Additional layers (Global Average Pooling, Batch Normalization, Dense) are added for task-specific adaptation.

<p>
  <img src="https://github.com/Ambatik-CH2-PS045/ambatik-machine-learning/blob/5a802d4419661b8c578f8a73f008c3d788f6267f/asset/model.PNG"/>
</p>

## Model Peformance

The trained model demonstrates strong performance on the provided dataset.

**Training Accuracy:** Achieved an impressive accuracy of 98.89% on the training dataset.

**Validation Accuracy:** Maintained a high validation accuracy of 92.04% on unseen validation data.

<p>
  <img src="https://github.com/Ambatik-CH2-PS045/ambatik-machine-learning/blob/5a802d4419661b8c578f8a73f008c3d788f6267f/asset/train.jpg"/>
</p>


## Additional Resources

All the dataset, trained model, and notebook can be found [here](https://drive.google.com/drive/folders/1_UTvftmA2APwfE5VTVOVNfnQBR6ZV7yV?usp=sharing)

# Ambatik Model Deployment Documentation
Embark on a journey of discovery: Study this documentation to uncover how to running Flask applications and uncover the machine learning models.

## Prerequisite

1. **Python:** `v3.10.6`

2. **Flask:** `v1.1.1`

## Getting Started:

1. Clone this [repository](https://github.com/Ambatik-CH2-PS045/ambatik-machine-learning.git)
   ```
   git clone https://github.com/Ambatik-CH2-PS045/ambatik-cloud-computing.git
   ```
   
2. If your Python version is different, run the following command
   ```
    sudo apt update
    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt update
    sudo apt install python3.9
    python3.9 --version
   ```
   
3. Install this following packages, by run this following command
   ```
    sudo apt install python3-pip
    pip install tensorflow
    pip install opencv-python
    pip install Flask
    pip install Pillow
    sudo apt install python3-flask
    sudo apt install gunicorn
   ```
4. Run the flask app with this command
   ```
   flask run
   ```
   If your flask app already run, it should show this message ` * Running on http://127.0.0.1:5000`
5. You can use the `/uploader` endpoint to directly access the flask for prediction

   **Request Form Data:**
   
   | Key | Type | Value |
   |---|---|---|
   | `file` | `file` | `file-name-example.jpg` |


6. Then you can run both of Node JS and Flask, if it success then when you use `/batik/predict` endpoint it will communicate to the flask and return the results of batik name and accuracy
