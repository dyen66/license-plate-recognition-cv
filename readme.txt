License Plate Detection and Recognition (ALPR)
An automated computer vision pipeline designed to detect vehicle license plates from images and extract alphanumeric text using deep learning-based Optical Character Recognition (OCR).
🚀 Overview
This project implements an end-to-end Automatic License Plate Recognition (ALPR) system. It combines traditional digital image processing techniques (OpenCV) for plate localization with modern deep learning models (EasyOCR/PyTorch) for character recognition.
Key Features
* Image Preprocessing: Noise reduction using Bilateral Filters to preserve edge integrity.
* Plate Localization: Intelligent contour detection and geometric filtering to isolate the plate region.
* Deep Learning OCR: High-accuracy text extraction using pre-trained EasyOCR models.
* Visual Verification: Automated bounding box and text overlay on the original source image.
🛠️ Tech Stack
* Language: Python
* Computer Vision: OpenCV (cv2), imutils
* Deep Learning: PyTorch, EasyOCR
* Visualization: Matplotlib, NumPy
📋 Implementation Pipeline
1. Grayscaling & Blurring: Convert image to grayscale and apply bilateral filtering to remove noise while keeping edges sharp.
2. Edge Detection: Utilize the Canny algorithm to identify the boundaries of objects.
3. Contour Filtering: Detect all shapes and sort them by area, searching for a four-sided polygon (the license plate).
4. Masking & Cropping: Isolate the detected plate area from the rest of the vehicle image.
5. Character Recognition: Pass the cropped plate image into EasyOCR to transcribe the text.


🖥️ Usage
You can run the detection pipeline through the provided Jupyter Notebook:
1. Open Plate Detection.ipynb.
2. Update the image path in the cv2.imread() cell.
3. Run all cells to see the step-by-step transformation and final result.
📊 Results
The system successfully localizes plates even in cluttered backgrounds and provides high-confidence text extraction for standard vehicle plates.
Original Image
	Detected Plate
	OCR Output