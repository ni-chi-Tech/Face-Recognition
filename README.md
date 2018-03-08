# Face Recognition
Using OpenCV inbuilt functions to recognize faces of my friends. The code is completely written in OpenCV using haarcascade detector to identify facial features. LBPH Face Recognizer is used to recognize difference between faces. LBPH (Local Binary Patterns Histogram) algorithm is used to identify faces.

## OpenCV Face Recognition
OpenCV has three built in face recognizers and thanks to OpenCV's clean coding, you can use any of them by just changing a single line of code. Below are the names of those face recognizers and their OpenCV calls.

  1. EigenFaces Face Recognizer Recognizer - ```cv2.face.createEigenFaceRecognizer()```
  2. FisherFaces Face Recognizer Recognizer - ```cv2.face.createFisherFaceRecognizer()```
  3. Local Binary Patterns Histograms (LBPH) Face Recognizer - ```cv2.face.createLBPHFaceRecognizer()```
We have got three face recognizers but do you know which one to use and when? Or which one is better? I guess not. So why not go through a brief summary of each, what you say? I am assuming you said yes :) So let's dive into the theory of each.

## EigenFaces Face Recognizer
This algorithm considers the fact that not all parts of a face are equally important and equally useful. When you look at some one you recognize him/her by his distinct features like eyes, nose, cheeks, forehead and how they vary with respect to each other. So you are actually focusing on the areas of maximum change (mathematically speaking, this change is variance) of the face. For example, from eyes to nose there is a significant change and same is the case from nose to mouth. When you look at multiple faces you compare them by looking at these parts of the faces because these parts are the most useful and important components of a face. Important because they catch the maximum change among faces, change the helps you differentiate one face from the other. This is exactly how EigenFaces face recognizer works.

## FisherFaces Face Recognizer
This algorithm is an improved version of EigenFaces face recognizer. Eigenfaces face recognizer looks at all the training faces of all the persons at once and finds principal components from all of them combined. By capturing principal components from all the of them combined you are not focusing on the features that discriminate one person from the other but the features that represent all the persons in the training data as a whole.

This approach has drawbacks, for example, images with sharp changes (like light changes which is not a useful feature at all) may dominate the rest of the images and you may end up with features that are from external source like light and are not useful for discrimination at all. In the end, your principal components will represent light changes and not the actual face features.

Fisherfaces algorithm, instead of extracting useful features that represent all the faces of all the persons, it extracts useful features that discriminate one person from the others. This way features of one person do not dominate over the others and you have the features that discriminate one person from the others.

## Local Binary Pattern Histogram Face Recognizer
As any other classifier, the Local Binary Patterns, or LBP in short, also needs to be trained on hundreds of images. LBP is a visual/texture descriptor, and thankfully, our faces are also composed of micro visual patterns. So, LBP features are extracted to form a feature vector that classifies a face from a non-face.

For each block, LBP looks at 9 pixels (3×3 window) at a time, and with a particular interest in the pixel located in the center of the window. Then, it compares the central pixel value with every neighbor's pixel value under the 3×3 window. For each neighbor pixel that is greater than or equal to the center pixel, it sets its value to 1, and for the others, it sets them to 0. After that, it reads the updated pixel values (which can be either 0 or 1) in a clockwise order and forms a binary number. Next, it converts the binary number into a decimal number, and that decimal number is the new value of the center pixel. We do this for every pixel in a block. Then, it converts each block values into a histogram, so now we have gotten one histogram for each block in an image. Finally, it concatenates these block histograms to form a one feature vector for one image, which contains all the features we are interested. So, this is how we extract LBP features from a picture.

## Execution
To execute the program, you need to install OpenCV in virtual environment.
To run the program just type in the following command in the terminal.
```bash
python main.py
```

## Solo Project
* [Nihar Chitnis](https://github.com/ni-chi), 16IT232
