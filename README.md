# Age-and-Gender-Estimation-using-Caffe
The dataset is divided into training and validation sets using Keras's `ImageDataGenerator` with a 20% split for validation. This setup ensures that `train_ds` contains 80% of the data for model training, while `valid_ds` comprises the remaining 20% for validation.


### Summary of `prediction.py`

The script `predict.py` is used for age and gender prediction using OpenCV and deep learning models. It captures video from a webcam, detects faces, and predicts the age and gender of the detected faces. The predictions are displayed on the video feed in real-time.

### Contents of `README.md`

```markdown
# Age and Gender Prediction

This project uses OpenCV and pre-trained Caffe models to predict the age and gender of faces detected in real-time from a webcam feed.

## Requirements

- Python 3.x
- OpenCV
- Numpy
- imutils

## Installation

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/age-gender-prediction.git
   ```
2. Navigate to the project directory
   ```bash
   cd age-gender-prediction
   ```
3. Install the required packages
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Ensure you have the required Caffe models and Haarcascade file in the `data` directory:
   - `deploy_age.prototxt`
   - `age_net.caffemodel`
   - `deploy_gender.prototxt`
   - `gender_net.caffemodel`
   - `haarcascade_frontalface_alt.xml`

2. Run the script
   ```bash
   python prediction.py
   ```

3. The webcam feed will open, and the detected faces will be displayed with their predicted age and gender.

## File Structure

- `prediction.py`: Main script to run the age and gender prediction.
- `data/`: Directory containing the model files and Haarcascade file.
  - `deploy_age.prototxt`
  - `age_net.caffemodel`
  - `deploy_gender.prototxt`
  - `gender_net.caffemodel`
  - `haarcascade_frontalface_alt.xml`

## How It Works

1. The script captures video from the webcam.
2. It uses the Haarcascade classifier to detect faces in the video feed.
3. For each detected face, it creates a blob and uses the pre-trained Caffe models to predict the age and gender.
4. The predictions are displayed on the video feed.

## License

This project is licensed under the MIT License.
```

### Additional Notes

- Ensure you have the Caffe model files and the Haarcascade XML file in the `data` directory.
- The script uses the following Caffe models:
  - Age prediction model: `deploy_age.prototxt` and `age_net.caffemodel`
  - Gender prediction model: `deploy_gender.prototxt` and `gender_net.caffemodel`
- Haarcascade file for face detection: `haarcascade_frontalface_alt.xml`

