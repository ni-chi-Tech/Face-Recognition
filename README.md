# Face Recognition
Using OpenCV inbuilt functions to recognize faces of my friends. The code is completely written in OpenCV using haarcascade detector to identify facial features. LBPH Face Recognizer is used to recognize difference between faces. LBPH (Local Binary Patterns Histogram) algorithm is used to identify faces.

## OpenCV Face Recognition
OpenCV has three built in face recognizers and thanks to OpenCV's clean coding, you can use any of them by just changing a single line of code. Below are the names of those face recognizers and their OpenCV calls.

  1. EigenFaces Face Recognizer Recognizer - ```python cv2.face.createEigenFaceRecognizer()```
  2. FisherFaces Face Recognizer Recognizer - ```python cv2.face.createFisherFaceRecognizer()```
  3. Local Binary Patterns Histograms (LBPH) Face Recognizer - ```python cv2.face.createLBPHFaceRecognizer()```
We have got three face recognizers but do you know which one to use and when? Or which one is better? I guess not. So why not go through a brief summary of each, what you say? I am assuming you said yes :) So let's dive into the theory of each.

## Execution
To execute the program, you need to install OpenCV in virtual environment.
To run the program just type in the following command in the terminal.
```bash
python main.py
```

## Solo Project
* [Nihar Chitnis](https://github.com/ni-chi), 16IT232
