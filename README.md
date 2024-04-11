# Face Recognition System
This project aims to implement a face recognition system for access control at the library. The system compares real-time images captured through a camera with a database of student photos to determine if an individual is authorized to access the library.

## Overview

The system consists of the following components:

## 1. Database Creation:

A database containing images of authorized students is required. Each student's folder in the database contains seven images of the student's face.

## 2. Model Creation:

The face recognition model is developed using Python. This model extracts features from the images in the database and compares them with features from newly captured images to determine the identity of the individual.

# Implementation Steps

## 1. Acquisition of Database Images

### 1.1. Libraries Importation

The required libraries for the project are imported:

- `face_recognition`: Python library for facial recognition.
- `cv2`: Open-source library for real-time image and video processing.
- `os`: Library for managing file system directories.

### 1.2. Data Access Function

A function '_get_data()' is defined to access the images in the database directory. This function returns the images along with their associated labels (student names).

## 2. Face Recognition Model Development

### 2.1. Image Recognition and Processing

The `Face_encoding(images_path, labels)` function is defined to collect features from the database images. The function converts images to grayscale and extracts facial features using `face_locations()` and `face_encodings()` functions. Student names are associated with the extracted features.

### 2.2. Comparison with Database Images

New images are captured through the webcam and processed for feature extraction. Features of the new image are compared with features of images in the database. If a match is found, the name of the recognized student is displayed; otherwise, "Unknown" is displayed.

## Testing

The system was tested with various images captured from the webcam to verify its functionality.

### Test Scenarios

- Testing with an image of a person not in the database.
- Testing with an image of a person in the database.

## Conclusion

The face recognition system successfully identifies authorized students based on the comparison of facial features with images stored in the database. This provides efficient access control for the library.
