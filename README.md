# Ambatik Cloud Computing Documentation
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
| `userid` | `text` | `1` |

6. Then you can run both of Node JS and Flask, if it success then when you use `/batik/predict` endpoint it will communicate to the flask and return the results of batik name and accuracy
