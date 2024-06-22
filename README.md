# YOLOv8 Android App

This repository contains an Android application utilizing a TensorFlow Lite model based on YOLOv8 for object detection.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Conversion](#model-conversion)
- [Model Details](#model-details)
- [TensorFlow Lite Integration](#tensorflow-lite-integration)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction

The YOLOv8 Android App is a mobile application that leverages the YOLOv8 model for real-time object detection. This project demonstrates the integration of TensorFlow Lite (TFLite) with an Android application to perform efficient and accurate object detection on mobile devices.

## Features

- Real-time object detection using YOLOv8
- Efficient processing with TensorFlow Lite
- User-friendly interface

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
2. Point your camera towards objects to detect them in real time.
3. Detected objects will be highlighted with bounding boxes and labels.

## Model Conversion

To convert the YOLOv8 model to TensorFlow Lite, follow the steps provided in the `model_conversion.ipynb` notebook available on Google Drive.

### Steps

1. **Open the notebook in Google Colab:**
    - Click the link to open the notebook: [model_conversion.ipynb](https://colab.research.google.com/drive/10RQCjBIc19sna2Nwa4oGso1aC17W8ARq?usp=sharing).

2. **Set up the environment:**
    The notebook will automatically install the necessary dependencies.

3. **Run the notebook:**
    Follow the instructions in the notebook to:
    - Export the YOLOv8 model.
    - Convert the exported model to TensorFlow Lite format.

4. **Download the TFLite model:**
    Once the conversion is complete, download the `.tflite` file.

5. **Move the TFLite model to the Android project:**
    - Navigate to the Android project directory: `app/src/main/assets/`.
    - Replace the existing `model.tflite` file with the downloaded `.tflite` file.
      * The default model in 'app/src/main/assets' is converted from [yolovn8.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov8n.pt).

## Model Details

The app uses a pre-trained YOLOv8 model converted to TensorFlow Lite format. YOLOv8 is known for its balance between speed and accuracy, making it suitable for mobile applications.

## TensorFlow Lite Integration

The input and output tensor formats of the TensorFlow Lite model are as follows:
- **Input tensor:** float32[1,640,640,3] or float32[1,3,640,640]
- **Output tensor:** float32[1,84,8400]

There is no longer a need to worry about tensor format or metadata issues that were previously encountered when using [TensorFlow Lite's object detection example for Android](https://github.com/tensorflow/examples/tree/master/lite/examples/object_detection/android).

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

- [YOLOv8](https://github.com/ultralytics/ultralytics) for the object detection model.
- [TensorFlow Lite](https://www.tensorflow.org/lite) for providing the framework to run the model on mobile devices.
- [Android Studio](https://developer.android.com/studio) for the development environment.
- [Google Colab](https://colab.research.google.com) for providing a cloud-based Jupyter notebook environment.
