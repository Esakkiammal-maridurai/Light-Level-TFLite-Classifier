# DAY--12

# Convert to TFLite – Light Level Classifier

## Project Description

This project demonstrates how to train a small TensorFlow neural network to classify light-level readings into three categories:

- Dark
- Normal
- Bright

The trained TensorFlow model is converted into a TensorFlow Lite (`.tflite`) model and tested using Python to verify that the TFLite model produces the same classification results as the original model.

## Objective

To train a TensorFlow model, convert it to TFLite format, and run inference on test light-level values.

## Technologies Used

- Python
- TensorFlow
- NumPy
- TensorFlow Lite
- Google Colab

## Light-Level Categories

| Light Level | Category |
|-------------|----------|
| 0 – 300 | Dark |
| 301 – 700 | Normal |
| 701 – 1000 | Bright |

## Model

A simple neural network with Dense layers and Softmax activation is used for classification.

### Training Configuration

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Epochs: 500
- Activation: ReLU and Softmax

## Training Data

The model is trained using sample light-level readings:

- 100, 150, 200 → Dark
- 400, 500, 600 → Normal
- 750, 850, 950 → Bright

## Test Data

The trained model is tested using:

- 150
- 500
- 900

## Prediction Results

| Light Level | Original Model | TFLite Model |
|------------:|----------------|--------------|
| 150 | Dark | Dark |
| 500 | Normal | Normal |
| 900 | Bright | Bright |

## TFLite Conversion

The trained TensorFlow model is converted into a `.tflite` file using the TensorFlow Lite Converter.

The generated file is:

`light_classifier.tflite`

## Result

The TFLite model successfully performs inference and produces the same classification results as the original TensorFlow model.

## Platform

Google Colab

## Files

- `light_level_classifier.ipynb` – Complete training, conversion, and inference notebook.
- `light_classifier.tflite` – Converted TensorFlow Lite model.

## Conclusion

This project demonstrates the process of training a TensorFlow classification model, converting it to TensorFlow Lite format, and verifying its predictions using test light-level values.
