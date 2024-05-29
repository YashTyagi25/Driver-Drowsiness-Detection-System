# Driver-Drowsiness-Detection-System
This project introduces a sophisticated machine learning system aimed at promptly identifying driver drowsiness to uphold road safety standards. By leveraging cutting-edge techniques in computer vision and data analysis, the system operates in real-time, continuously monitoring driver behavior and physiological indicators.

Through the fusion of various sensory inputs, including facial expressions, eye movements, and vehicle dynamics, the system detects early signs of drowsiness, alerting the driver and activating safety measures to prevent potential accidents. The implementation of this system holds significant promise in reducing road fatalities and enhancing overall transportation safety.

 Tech Stack Used:

    1. OpenCV: OpenCV (Open Source Computer Vision Library) is utilized for image and video processing tasks, such as reading frames from a video capture, converting color spaces, and drawing annotations on images.
    2. dlib: dlib is employed for face detection and facial landmark localization. It provides pre-trained models for these tasks, such as the frontal face detector and the shape predictor used in this code.
    3. NumPy: NumPy is utilized for numerical operations and array manipulation. It's used here to convert facial landmarks into NumPy arrays for easier processing.
    4. scikit-learn: scikit-learn is used for evaluating the performance of the drowsiness detection system. It provides metrics such as accuracy, precision, recall, and F1-score, as well as tools for generating a 
       confusion matrix.
       
 How it is Used:

    1. Face Detection: The code begins by capturing frames from a video feed (presumably from a webcam) using OpenCV. It then utilizes dlib's face detector to locate faces in each frame.
    2. Facial Landmark Detection: Once a face is detected, the code employs a pre-trained shape predictor from dlib to localize facial landmarks, specifically the coordinates of the eyes.
    3. Eye Aspect Ratio (EAR) Calculation: With the eye landmarks identified, the code calculates the Eye Aspect Ratio (EAR) for each eye, which is a measure used to detect drowsiness based on eye closure.
    4. Visualization: It draws the detected eyes on the frame using OpenCV, highlighting the regions of interest.
    5. Drowsiness Detection: Based on the calculated EAR, the code determines whether the driver is drowsy. If the average EAR falls below a certain threshold (0.25 in this case), the code labels the driver as 
       drowsy and displays a warning on the frame.

