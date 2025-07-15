# Automatic Number Plate Recognition (ANPR)

## Project Description

This Python script implements an Automatic Number Plate Recognition (ANPR) system. It processes an image to detect a car number plate, extracts the region of interest, and then uses Optical Character Recognition (OCR) to read the text displayed on the plate. The process involves image pre-processing, contour detection, and text recognition.

## Features

* **Image Loading:** Loads a local image file for processing.
* **Image Pre-processing:** Converts image to grayscale, applies bilateral filtering for noise reduction while preserving edges, and performs Canny edge detection.
* **Number Plate Localization:** Uses contour detection and polygonal approximation to find the most probable rectangular area corresponding to a number plate.
* **Region of Interest (ROI) Cropping:** Crops the detected number plate area from the image.
* **Optical Character Recognition (OCR):** Integrates EasyOCR to accurately read characters from the cropped number plate image.
* **Visualization:** Displays intermediate processing steps (grayscale, filtered, edged, masked, cropped images) and the final output with the detected text and a bounding box on the original image.

## Prerequisites

Before running this script, ensure you have the following installed:

* Python 3.x
* **OpenCV:** `pip install opencv-python`
* **Matplotlib:** `pip install matplotlib`
* **NumPy:** `pip install numpy`
* **EasyOCR:** `pip install easyocr`
    * *Note:* EasyOCR relies on PyTorch. Depending on your system, you might need to install PyTorch separately. Refer to the [EasyOCR GitHub page](https://github.com/JaidedAI/EasyOCR) for detailed installation instructions if you encounter issues.
* **Imutils:** `pip install imutils`

## Installation and Setup

1.  **Clone the repository (or download the script):**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
    (Replace `your-username` and `your-repo-name` with your actual GitHub details.)

2.  **Place your test image:**
    The script currently expects a test image at a hardcoded path.
    **Update line 9:** `img = cv2.imread("C:/Users/ayush/Downloads/Test 3.jpg")`
    Change `"C:/Users/ayush/Downloads/Test 3.jpg"` to the actual path of the image you want to process, or place your image in the same directory as the script and update the path accordingly (e.g., `"Test 3.jpg"`).

## Usage

To run the number plate recognition script:

```bash
python number_plate_recog.py
