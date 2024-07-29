# 🛠️ Industrial Tool Anomaly Detection

Welcome to the **Industrial Tool Anomaly Detection** project! This repository contains code and resources for detecting anomalies in industrial tools using computer vision techniques. 

## 🏗️ Introduction

This project leverages computer vision to identify anomalies in industrial tools. The approach includes detecting and comparing contours, distances, and shapes of tools to determine any deviations or anomalies.

## ✨ Features

- 📏 Calculate distances between key points on the tool.
- 🔍 Match shapes using ORB feature detection.
- ✅ Accept or reject tools based on comparison metrics.
- 🖼️ Visualize bounding boxes and key points on the images.

## ⚙️ Installation

To get started with the project, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/IndustrialToolAnomalyDetection.git
    ```

2. **Navigate to the project directory:**
    ```bash
    cd IndustrialToolAnomalyDetection
    ```
3. **Install necessary libraries**
   ```bash
    pip install numpy opencv-python matplotlib
    ```
   
5. **Place your images**
   Ensure you have your reference image (frame_0.jpg) and the image you want to analyze (e.g., frame_100.jpg) in the same directory as your script.

## 🚀 Usage

To run the anomaly detection, use the `driver` function with your image file:

1. **Import the required functions:**
    ```python
    from main import driver
    ```

2. **Run the detection:**
    ```python
    result = driver("path_to_your_image.jpg")
    print(result)  # This will print True if no anomaly is found, otherwise False
    ```

## 🛠️ Functions

### `uppertooth(img)`

Calculates the distance between the uppermost and lowermost points of the contours.

### `lowertooth(img)`

Calculates the distance between the second uppermost and second lowermost points of the contours.

### `match(img1, img2='frame_0.jpg')`

Matches the shapes of two images using ORB feature detection and returns "accepted" if the images match, otherwise "rejected".

### `driver(img)`

Main function that uses the above functions to determine if the tool in the image has any anomalies.

## 🤝 Contributing

We welcome contributions to enhance the capabilities of this project! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Push the branch and open a pull request.
