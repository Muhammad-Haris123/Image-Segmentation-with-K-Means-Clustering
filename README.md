This project implements interactive image segmentation using K-Means clustering. It includes two approaches: one using the built-in KMeans from scikit-learn, and the other using a custom KMeans function.

Table of Contents
1. Introduction
2. Dependencies
3. Project Structure
4. Usage
5. Methodology
6. Built-in KMeans
7. Custom KMeans
8. Results

Introduction
Image Segmentation with K-Means Clustering is an image segmentation tool that separates the foreground from the background using color-based seed pixels. The segmentation process is refined using K-Means clustering to identify similar regions in the image, making it interactive and efficient.

Dependencies
1. Python 3.x
2. OpenCV (cv2)
3. NumPy
4. scikit-learn (sklearn)

Install the dependencies with:
pip install opencv-python numpy scikit-learn

Project Structure
1. main.py: Main script for both built-in and custom KMeans approaches.
2. Q1 Dataset/: Folder containing the input images (lady.png, lady stroke 1.png, lady stroke 2.png).

Methodology
Built-in KMeans
1. Read the original image and auxiliary image.
2. Convert auxiliary image to HSV for more reliable color detection.
3. Create masks for foreground (red) and background (blue) colors.
4. Use scikit-learn's KMeans to cluster the seed pixels.
5. Generate a segmentation mask based on cluster likelihoods.

Custom KMeans
1. Extract seed pixels using multiple stroke images.
2. Implement a custom KMeans function.
3. Generate the segmentation mask based on pixel distances to cluster centers.