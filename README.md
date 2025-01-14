# Python-Based Face Recognition Application Using TensorFlow and OpenCV

## 1. Introduction
Face recognition has emerged as a transformative technology in computer vision, enabling applications in security, personalization, and user authentication. This project focuses on creating a real-time face recognition application leveraging a pre-trained model exported from Google Teachable Machine. Integration with OpenCV allows for real-time image capture and processing, making the application highly interactive and efficient.

## 2. Objective
The key objectives of this project are:

- To implement a face recognition system using a pre-trained TensorFlow Lite model.
- To integrate real-time webcam feeds using OpenCV for dynamic face recognition.
- To preprocess input data for compatibility with the pre-trained model and provide accurate predictions.

## 3. Tools and Technologies
### Programming Language
- Python

### Libraries and Frameworks
- TensorFlow Lite for model inference.
- OpenCV for webcam integration and image preprocessing.
- NumPy for numerical operations.

### Hardware
- GPU support (optional) for optimized inference.

## 4. Methodology
### 4.1 Training the Model
Training a model using Google’s Teachable Machine is simple and beginner-friendly. Follow these steps:

1. **Access Teachable Machine**: Visit the [Teachable Machine](https://teachablemachine.withgoogle.com/) website.
2. ![image](https://github.com/user-attachments/assets/0fc2e429-bb55-4d81-9fa5-006945660cb9)


3. **Choose a Project Type**: Select the type of model to train (e.g., Image Project).
4. ![image](https://github.com/user-attachments/assets/d34fbc1a-de62-4f1d-a784-4a78bca87c21)


5. **Upload or Capture Data**:
   - Upload images from your device.
   - Alternatively, use your webcam to capture photos directly into each class.
![image](https://github.com/user-attachments/assets/cc39061b-c53c-4d88-a11a-1d78435ae2fd)

6. **Train the Model**:
   - Once you have sufficient data for each class, click the "Train Model" button.
   - Teachable Machine will process the data and train a model based on your inputs.
![image](https://github.com/user-attachments/assets/848864e6-c83d-46df-becd-cf5ccb83b9b9)


7. **Test the Model**: Test your model by providing new inputs to evaluate its accuracy.
![image](https://github.com/user-attachments/assets/b67aaaa6-daea-4782-9a7b-a98a3f88c42b)


9. **Export the Model**:
   - Export the trained model (e.g., TensorFlow format) for further use.
![image](https://github.com/user-attachments/assets/d98ee1f7-5af9-4d31-a944-3247014d6c1a)

### 4.2 Downloading and Setting Up
1. **Download the Files**:
   - Export the trained model and download the associated files (e.g., `keras_Model.h5`, `labels.txt`).

2. **Organize the Files**:
   - Ensure the model and labels files are in the same directory as the Python script.

3. **Install Dependencies**:
   - Install required libraries using the following commands:
     ```bash
     pip install tensorflow==2.10.0
     pip install opencv-python==4.5.5.64
     pip install numpy==1.21.6
     ```

4. **Run the Application**:
   - Execute the Python script to launch the application.

### 4.3 Real-Time Face Recognition
1. **Model Loading**:
   - The `keras_Model.h5` file is loaded using TensorFlow's Keras API for inference.

2. **Webcam Integration**:
   - OpenCV’s `VideoCapture` initializes the webcam for live video feeds.

3. **Image Preprocessing**:
   - Frames are resized to match the model’s input size (e.g., 224x224 pixels).
   - Images are normalized to the range [-1, 1].

4. **Prediction and Output**:
   - Predictions are made using the model, and class labels with confidence scores are displayed in real-time.

5. **Exit Condition**:
   - Press the `Esc` key to stop the application.

### 4.4 Code Explanation
Here is a brief explanation of the script:

- **Import Libraries**:
  - TensorFlow, OpenCV, and NumPy are used for model inference, webcam integration, and numerical computations.

- **Load Model and Labels**:
  - The trained model and class labels are loaded from `keras_Model.h5` and `labels.txt`.

- **Webcam Feed**:
  - The script captures frames in real-time using OpenCV and processes them for predictions.

- **Prediction Loop**:
  - Frames are resized, normalized, and passed to the model for classification.
  - The class with the highest confidence score is displayed along with the score.

- **Exit Mechanism**:
  - Press the `Esc` key to terminate the application and release resources.

## 5. Challenges and Solutions
### Challenges
1. **Model Compatibility**: Ensuring TensorFlow Lite models align with the framework’s inference requirements.
2. **Webcam Initialization**: Handling potential issues with webcam access.
3. **Performance Optimization**: Balancing real-time processing with model accuracy.

### Solutions
- Validated models for compatibility.
- Incorporated robust error handling for webcam integration.
- Optimized preprocessing for faster inference.

## 6. Results
The application can:

- Capture real-time frames from the webcam.
- Preprocess frames for inference.
- Display predicted class labels and confidence scores in real-time.

## 7. Future Scope
### Model Enhancements
- Train on larger, more diverse datasets.
- Enable multi-class and multi-face detection.

### User Interface
- Build a web interface with Flask or Streamlit.
- Add interactive GUI elements.

### Deployment
- Host on cloud platforms for accessibility.
- Integrate advanced features like emotion detection.

## 8. Conclusion
This project showcases the effective use of TensorFlow Lite and OpenCV for real-time face recognition. Its modular design allows for further enhancements, making it a robust foundation for advanced applications.

---

**Contribution**
Project by Jayanth M. Contributions and feedback are welcome for further improvements. For detailed documentation and updates, visit the project repository.


