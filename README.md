
## **Optical Character Recognition (OCR) System**
# Optical Character Recognition (OCR) System using OpenCV & Tesseract

## Introduction

Optical Character Recognition (OCR) is a computer vision technique that enables machines to **identify and extract text from images** and convert it into **machine-readable digital text**.

This project implements a **complete OCR pipeline** using:

* **OpenCV** for image preprocessing
* **Tesseract OCR** for text recognition

The system focuses on improving OCR accuracy by applying **image enhancement techniques before recognition**, which is a critical step in real-world OCR applications.

## Project Objectives

* To design a complete OCR pipeline from image input to text output
* To understand the importance of preprocessing in OCR accuracy
* To extract printed text from real-world images
* To convert image-based documents into editable text format
## Why This Project Is Important

OCR systems are widely used in:

* Document digitization (books, notes, PDFs)
* Invoice and bill processing
* ID card and certificate verification
* Assistive technologies for visually impaired users
* Banking and government automation systems

## Technologies & Tools Used

### Programming Language

* **Python**

### Libraries

* **OpenCV** – Image preprocessing
* **pytesseract** – Python wrapper for Tesseract OCR
* **NumPy** – Image matrix operations
* **Matplotlib** – Visualization

### OCR Engine

* **Tesseract OCR (Open Source)**

### Platform

* **Google Colab** (primary)
* **Local System** (optional)
## Project Directory Structure
│
├── ocr_system.ipynb
├── sample_images/
│   ├── invoice.jpg
│   ├── book_page.jpg
│   └── signboard.png
│
├── extracted_text/
│   └── extracted_text.txt
│
└── README.md


## System Architecture

Input Image
     ↓
Image Preprocessing
     ↓
Text Recognition (Tesseract OCR)
     ↓
Extracted Text Output

## Detailed Methodology

### Image Acquisition

* Input image is uploaded by the user
* Image can be a scanned document, book page, or printed text image

### Image Preprocessing (MOST IMPORTANT STEP)

Preprocessing is done to enhance text visibility and reduce noise.

#### a) Grayscale Conversion

* Converts RGB image to grayscale
* Reduces computational complexity

#### b) Noise Removal

* Gaussian Blur is applied
* Removes small dots and distortions

#### c) Thresholding

* Separates text from background
* Converts image to binary (black & white)
* Improves OCR accuracy significantly
###  OCR using Tesseract

* Preprocessed image is passed to Tesseract
* OCR engine analyzes character shapes
* Extracts text based on trained language models

**Configuration Used:**

* OEM (OCR Engine Mode)
* PSM (Page Segmentation Mode)

### Output Generation

* Extracted text is displayed on screen
* Text is saved into a `.txt` file
* File can be downloaded for further use

## Features Implemented

Printed text recognition
Image preprocessing pipeline
Text extraction and storage
Modular and extendable design
Works on different document types

## How to Run the Project (Google Colab)

### Install Dependencies

pip install pytesseract opencv-python numpy matplotlib


### Execution Steps

1. Upload an image with printed text
2. Run preprocessing steps
3. Apply OCR using Tesseract
4. View and download extracted text


## Experimental Results & Observations

### Works Best For:

* High-resolution images
* Clear printed text
* High contrast between text and background

### Performance Degrades For:

* Handwritten text
* Blurry or low-quality images
* Poor lighting conditions

## Limitations

* Does not handle handwritten text effectively
* Sensitive to noise and illumination
* Requires preprocessing tuning for different image types
* Not layout-aware (tables and forms need advanced OCR)

## Future Enhancements

* Handwritten text recognition using deep learning
* Multilingual OCR support
* Table and form extraction
* PDF document OCR
* Integration with web or mobile applications


##  Learning Outcomes

* Understanding OCR workflow and pipeline
* Practical experience with OpenCV preprocessing
* Hands-on exposure to Tesseract OCR
* Knowledge of real-world document automation systems
