Here's a README file for your Flask-based Attendance System project:

---

# Flask Attendance System with Face Recognition

This project is a Flask-based web application for an automated attendance system using face recognition. The system captures faces using a webcam, trains a KNN model, and identifies users to mark their attendance. 

## Features

- **Automated Attendance**: The system automatically marks attendance by recognizing faces.
- **Face Detection and Recognition**: Uses OpenCV for face detection and a K-Nearest Neighbors (KNN) model for face recognition.
- **Real-Time Processing**: Captures video from a webcam, processes it in real-time, and displays the results.
- **User Management**: Allows adding new users with their faces to the system.
- **Attendance Record**: Stores attendance records in a CSV file.

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/attendance-system.git
   cd attendance-system
   ```

2. **Install dependencies**:

   Make sure you have Python installed, then run:

   ```bash
   pip install -r requirements.txt
   ```

   Required packages include:
   - Flask
   - OpenCV (`opencv-python`)
   - Scikit-learn
   - Numpy
   - Pandas
   - Joblib

3. **Prepare directories**:

   Ensure the following directories exist:

   ```bash
   mkdir -p Attendance static/faces
   ```

   The system will automatically create these directories if they do not exist.

4. **Download pre-trained models**:

   Download the `haarcascade_frontalface_default.xml` file from the [OpenCV GitHub repository](https://github.com/opencv/opencv/tree/master/data/haarcascades) and place it in the project root.

## Usage

1. **Run the Flask app**:

   ```bash
   python app.py
   ```

2. **Access the application**:

   Open your web browser and navigate to `http://127.0.0.1:5000/`.

3. **Add new users**:

   - Go to the `/add` route.
   - Enter a username and user ID.
   - Capture images using the webcam by following the instructions.
   - The system will automatically train the model with the new user's data.

4. **Start attendance**:

   - Go to the `/start` route.
   - The system will start capturing video and recognizing faces to mark attendance.

5. **View Attendance**:

   - Visit the homepage (`/`) to view the list of users who have marked attendance.

## Project Structure

- **app.py**: Main Flask application.
- **templates/**: HTML templates for the Flask application.
- **static/**: Static files including saved face images and the trained model.
- **Attendance/**: Folder to store the attendance CSV files.

## Dependencies

Ensure you have the following Python packages installed:

- Flask
- OpenCV
- Scikit-learn
- Numpy
- Pandas
- Joblib

##
