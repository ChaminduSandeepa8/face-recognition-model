Markdown

# Real-Time Face Recognition System 📷

A simple, efficient, and real-time face recognition system built using Python and OpenCV. This project detects and identifies faces through a live webcam feed by comparing them against a pre-encoded dataset.

## 🚀 Features
* **Real-Time Recognition:** Processes live video feed to detect and recognize faces instantly.
* **Optimized Performance:** Uses frame resizing techniques to ensure smooth running without lag, even on standard hardware.
* **Privacy-Focused:** Personal image datasets and trained model files (`.pickle`) are excluded from the repository using `.gitignore`.
* **Accuracy:** Utilizes the powerful `face_recognition` library (built on dlib) for highly accurate face encodings and distance measurements.

## 🛠️ Technologies Used
* **Python 3**
* **OpenCV (`cv2`)** - For handling webcam feed and image processing.
* **Face_recognition** - For generating 128-d face encodings and matching logic.
* **NumPy** - For mathematical operations and array handling.
* **Pickle** - For serializing and saving the trained face data.

## 📁 Project Structure
* `notebook.ipynb` / `notebook22.ipynb`: Jupyter notebooks containing the logic for dataset creation, face encoding, and real-time recognition.
* `data_set/`: (Ignored via git) Directory containing user images categorized by folders.
* `face_encodings.pickle`: (Ignored via git) The serialized file containing generated face encodings and names.

## 💡 How It Works
1. **Dataset Creation:** The system reads images from the `data_set` folder and generates a unique 128-dimension encoding for each face.
2. **Encoding Storage:** These encodings, along with the corresponding names, are saved into a binary file (`face_encodings.pickle`) for quick loading.
3. **Live Detection:** The webcam captures live frames, which are then resized for speed. The system detects faces in the frame, calculates their encodings, and compares them with the saved data.
4. **Matching:** If the "face distance" (difference) is below the strict threshold (0.6), the person is recognized, and their name is displayed on the screen with a bounding box.

## ⚙️ Setup & Installation
1. Clone this repository:
   ```bash
   git clone [https://github.com/ChaminduSandeepa8/face-recognition-model.git](https://github.com/ChaminduSandeepa8/face-recognition-model.git)

    Navigate to the project directory:
    Bash

    cd face-recognition-model

    Install the required dependencies:
    Bash

    pip install opencv-python face_recognition numpy

    (Note: Installing face_recognition may require cmake and a C++ compiler to be installed on your system).

Developed as a learning project to explore Computer Vision and AI.