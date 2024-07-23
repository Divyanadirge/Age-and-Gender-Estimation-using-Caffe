# Age-and-Gender-Estimation-using-Caffe
The dataset is divided into training and validation sets using Keras's `ImageDataGenerator` with a 20% split for validation. This setup ensures that `train_ds` contains 80% of the data for model training, while `valid_ds` comprises the remaining 20% for validation.


# Predict Age and Gender using OpenCV and Deep Learning

This repository contains a Python script to predict age and gender using OpenCV and deep learning models.

## Requirements

- OpenCV
- imutils
- numpy

## Installation

1. Install OpenCV:
   ```sh
   pip install opencv-python
   ```

2. Install other required libraries:
   ```sh
   pip install imutils numpy
   ```

3. Download the pre-trained models:
   - `deploy_age.prototxt`
   - `age_net.caffemodel`
   - `deploy_gender.prototxt`
   - `gender_net.caffemodel`
   - `haarcascade_frontalface_alt.xml`

   Ensure these files are placed in the `data` directory.

## Usage

Run the script to start the age and gender prediction:
```sh
python prediction.py
```

## Script Overview

The script initializes the Caffe models for age and gender prediction, captures video from the webcam, detects faces, and predicts the age and gender for each detected face.

### Functions

- `initialize_caffe_models()`: Loads the pre-trained Caffe models for age and gender prediction.
- `read_from_camera(age_net, gender_net)`: Captures video from the webcam, detects faces, and uses the loaded models to predict age and gender.

### Model Mean Values and Lists

- `MODEL_MEAN_VALUES`: Mean values for the models.
- `age_list`: List of age ranges.
- `gender_list`: List of genders.

### Main Flow

1. Initialize the models.
2. Start capturing video.
3. Detect faces in each frame.
4. For each detected face:
   - Predict gender.
   - Predict age.
   - Overlay the predicted gender and age on the video frame.
5. Display the video frame.
6. Press 'q' to quit.









