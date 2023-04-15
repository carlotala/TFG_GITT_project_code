# TFG GITT:

This repository contains the code for the undergraduate thesis project of Carlota López Argote: **Evaluation of Deep Learning techniques for anomaly detection in rotating machinery**.

### Data:
The data used for this project can be downloaded from https://mb.uni-paderborn.de/en/kat/main-research/datacenter/bearing-datacenter/data-sets-and-download
. The dataset consists of time-series vibration measurements from bearings in a rotating machine, with both normal and faulty conditions.

### Requirements:
There is a **requirements.txt** file that lists all the dependencies needed to run the project. To install them, run:

```python
pip install -r requirements.txt
```

### Code Structure:
The code is organized into the following Jupyter notebooks:

1. load_data.ipynb: This notebook loads and preprocesses the data for use in the classification models.
2. CNN_Model.ipynb: This notebook implements and trains a Convolutional Neural Network (CNN) model for classification, and provides analysis of the results.
3. RL_CNN_Model.ipynb: This notebook implements and trains a Deep Q-Network (DQN) model for classification, and provides analysis of the results.
4. join_models.ipynb: This notebook combines the predictions of the CNN and DQN models to create a more robust classification model, and provides analysis of the results.

Please run the notebooks in the order specified above.

### Using the trained models:
The trained models are available in the `/models` directory in the form of .h5 files. To use them for inference, you can load them using the following code snippet in Python:

```python
import tensorflow as tf

# Load the CNN model
cnn_model = tf.keras.models.load_model('models/cnn_model_6.h5')

# Load the DDQN model
ddqn_model = tf.keras.models.load_model('models/ddqn_model_14.h5')
```

### Usage:
To use this code, simply clone this repository to your local machine and open the desired Jupyter notebook(s) in a Python environment with the required libraries installed. Follow the instructions in each notebook to load the data, train the model(s), and analyze the results.

Please note that the data must be downloaded and prepared separately before running the code.
