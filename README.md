Cabs Fare Prediction

Project Description

This project aims to predict cab fares using a dataset that includes trip details and corresponding weather information. It utilizes a deep learning model built with TensorFlow and Keras to account for various factors influencing the final fare, including time of day, trip distance, and weather conditions.

Key Features

  * **Data Source:** The model is trained on a dataset from a file named `taxi_with_weather (1).csv`.
  * **Feature Engineering:** The notebook extracts time-based features (pickup/drop-off hour, day of the week) and creates a `Condition_Code` to represent weather conditions numerically. A new `new_fare_amount` column is also created, which applies a 10% fare increase for certain weather conditions like rain or snow.
  * **Preprocessing:** The data is cleaned by removing rows with missing values. Quantile normalization is then applied to the selected features before splitting the data into training and testing sets.
  * **Model Architecture:** The project uses a sequential deep learning model with multiple dense layers, employing `LeakyReLU` for activation, `BatchNormalization`, and `Dropout` layers to prevent overfitting.
  * **Training:** The model is compiled using the `Adam` optimizer and a custom `pseudo_huber_loss` function. It also includes a `ReduceLROnPlateau` callback to adjust the learning rate during training.

Getting Started
Prerequisites

This project requires the following Python libraries. You can install them using pip:

```bash
pip install pandas numpy scikit-learn tensorflow keras
```
Running the Notebook

1.  Clone this repository to your local machine.
2.  Ensure you have the `taxi_with_weather (1).csv` dataset in the same directory as the notebook.
3.  Open the `Cabs_fare_prediction (2).ipynb` file in a Jupyter environment.
4.  Run the cells sequentially to perform data loading, preprocessing, model training, and evaluation.

-----
Project Structure

  * `Cabs_fare_prediction (2).ipynb`: The Jupyter notebook containing the full project code.
  * `taxi_with_weather (1).csv`: The dataset used for the project.

