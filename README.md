![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&width=1000&height=200&section=header&text=Machine%20Learning%20Training%20Bot&fontSize=30&fontColor=black)

<!-- header is made with: https://github.com/kyechan99/capsule-render -->

[John Sung](https://linkedin.com/in/john-sung-3675569) [<img src="https://cdn2.auth0.com/docs/media/connections/linkedin.png" alt="LinkedIn -  John Sung" width=15/>](https://linkedin.com/in/john-sung-3675569/)

                                                             
<br>
Columbia FinTech Bootcamp Assignment - Module 14

---

### Table of Contents

* [Overview](#overview)
* [Requirements](#requirements)
* [Data](#data)
* [Visualization](#visualization)
* [License](#license)

---

## Overview

In this program, a model that predicts whether applicants will be successful if funded by Alphabet Soup was created. The CSV file used contains more than 34,000 organizations that have received funding from Alphabet Soup over the years to work with. With the knowledge of machine learning and neural networks the following was performed...

* Prepare the data for use on a neural network model.

* Compile and evaluate a binary classification model using a neural network.

* Optimize the neural network model.
 
---

## Requirements

This project leverages python 3.7, scikit-learn, TemsorFlow and Keras.

A [conda](https://docs.conda.io/en/latest/) environment with liabraries listed below and [Jupyter Notebook/Lab](https://jupyter.org/) are required to run the code.

The following libraries were used:

1. [TensorFlow 2.0](https://www.tensorflow.org/) - The core open source library to help you develop and train ML models.
2. [Scikit Learn](https://scikit-learn.org/stable/index.html) - Scikit Learn or Sklearn is one of the most used Python libraries for Data Science, along with others like Numpy, Pandas, Tensorflow, or Keras.


Install the following librarie(s) in your terminal...

    pip install -U scikit-learn
    pip install --upgrade tensorflow

---

## Data

The data used in this neural network model was from derived from a CSV file called applicants_data.csv.:

---

## Visualization

Uploading and reading the .csv file
![readcsv](Images/read_csv.PNG)

Creating a OneHotEncoder instance
![onehotencoder](Images/onehotencoder.PNG)

Fitting the model using 100 epochs and the training data
![fitmodel](Images/fit_model_100_epochs.PNG)

Displaying the accuracy scores achieved by each model and comparing the results
![three_models](Images/model_loss_model_accuracy_three_models.PNG)

Saving alternative models as an HDF5 file.
![altmodels](Images/alt_models_HDF5.PNG)

---

## License

MIT


