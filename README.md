# YOLOv8 Android App

This repository contains an Android application utilizing a TensorFlow Lite model based on YOLOv8 for object detection.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Usage](#usage)
- [Model Conversion](#model-conversion)
- [Model Details](#model-details)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction

The YOLOv8 Android App is a mobile application that leverages the YOLOv8 model for real-time object detection. This project demonstrates the integration of TensorFlow Lite (TFLite) with an Android application to perform efficient and accurate object detection on mobile devices.

## Features

- Real-time object detection using YOLOv8
- Efficient processing with TensorFlow Lite
- User-friendly interface

## Screenshots

some screenshots of the app

## Installation

### Prerequisites

- Android Studio
- Android device or emulator

### Steps

1. **Clone the repository:**
    ```bash
    git clone https://github.com/superbabii/YOLOv8-AndroidApp.git
    cd YOLOv8-AndroidApp
    ```

2. **Open the project in Android Studio:**
    - Open Android Studio and select `Open an existing Android Studio project`.
    - Navigate to the cloned repository and open it.

3. **Build and run the project:**
    - Connect your Android device or start an emulator.
    - Click `Run` in Android Studio.

## Usage

1. Open the app on your device.
2. Point your camera towards objects to detect them in real-time.
3. Detected objects will be highlighted with bounding boxes and labels.

## Model Conversion

To convert the YOLOv8 model to TensorFlow Lite, follow the steps provided in the `model_conversion.ipynb` notebook included in this repository.

### Steps

1. **Set up the environment:**
    Ensure you have Python and the necessary libraries installed. You can install the required libraries using:
    ```bash
    pip install -r requirements.txt
    ```

2. **Run the Jupyter Notebook:**
    Open and run the `model_conversion.ipynb` notebook. This notebook will guide you through the process of:
    - Exporting the YOLOv8 model.
    - Converting the exported model to TensorFlow Lite format.

3. **Move the TFLite model to the Android project:**
    Once the conversion is complete, place the `.tflite` file in the `assets` directory of your Android project.

## Model Details

The app uses a pre-trained YOLOv8 model converted to TensorFlow Lite format. YOLOv8 is known for its balance between speed and accuracy, making it suitable for mobile applications.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [YOLOv8](https://github.com/ultralytics/yolov8) for the object detection model.
- [TensorFlow Lite](https://www.tensorflow.org/lite) for providing the framework to run the model on mobile devices.
- [Android Studio](https://developer.android.com/studio) for the development environment.
