# lane-line-detection

# Lane Lines Detection - CSC 481 Fall 2023 Final Report

## Author
- **Jashwanth Neeli**
- Department of Data Science, DePaul University, Chicago, Illinois, USA
- Email: jneeli@depaul.edu

## Abstract
The main objective of this project is to determine a real-time curve value to aid drivers or autonomous vehicles in making necessary turns to stay on the road. This paper explores methods for detecting lane lines on unmarked roads using solely vision or camera data based on digital image processing techniques.

## Introduction
Lane line detection is crucial for autonomous vehicle systems, enabling safe and effective navigation by understanding lane lines on roads. This project involves using image processing techniques and algorithms like Canny edge detection and Hough transform, providing practical experience with OpenCV and insights into image processing.

## Background
The project involves implementing edge detection using various techniques like canny edge detection, gaussian, and grayscale to enhance object visibility. Different color selection techniques (RGB, HSV, HSL) were also experimented with to identify the best method for detecting lane lines.

## Methods
Our test image dataset, sourced from Kaggle, features images with slight distortions due to the camera lens used. The images vary in road color and surroundings, with the camera fixed at the front of the car.

## Experiments
- **Color Selection**: Applied to retain white and yellow lane lines while blacking out other elements in RGB, HSV, and HSL color spaces.
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/eca02afc-4635-4297-874c-41d65049e547)
- **HSV color**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/17a88bfa-24ec-4767-acb7-9d34018aa8c1)
- **HSL**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/fef9ce21-00ba-4341-b017-15f92132f32b)
- **HSL color selection**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/c039e7eb-54cb-4423-917f-866feff8071f)

- **Edge Detection**: Implemented using grayscale conversion and Gaussian smoothing, followed by Canny edge detection.
- **gray scale**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/97169386-ed96-4171-b398-77a6c5f7c78f)
- **gaussian smoothing**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/e618b748-bbf5-4b7f-be9d-bd27d950fed8)
- **canny edge detection**:
  ![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/0190074c-943f-4c59-9aaa-afc6c8a2143e)

- **Region of Interest**: Focused on areas typically containing lane lines by defining and applying a mask to cut out these regions.
![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/ac30b179-5426-4a49-8444-24926111ef67)

## Hough Transform
Used to detect lines in the image, the Hough Transform identifies lines represented by their endpoints. This helps in isolating features of a particular shape within an image, crucial for lane detection.
![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/32dd7ef2-dfcc-4dad-b7f5-afcff4d8b5cd)

## Averaging and Extrapolating Lane Lines
Detected multiple lines for each lane line were averaged and extrapolated to represent single lines for each lane, improving the clarity and accuracy of the detection.
![image](https://github.com/jashwanthneeli/lane-line-detection/assets/76511089/8ea0827e-590a-46be-9ded-1db23307cadb)

## Application on Video Streams
The aforementioned functions were applied to video streams to detect lane lines in real-time, demonstrating the practical application of the developed techniques.

## Conclusion
The project successfully demonstrates the use of Hough transform for detecting lane lines in simple scenarios, providing a foundational approach to lane detection that can be expanded for more complex environments.

