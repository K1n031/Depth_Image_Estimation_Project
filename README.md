# Depth Image Estimation Project

## Overview
This project focuses on developing a depth estimation system using stereo image pairs. The system uses different image matching techniques, including pixel-wise and window-based matching, to estimate the depth of objects in the images.

## Table of contents
* Installation
* Usage
* Project Structure
* Methodology
* Results

## Installation
### Prerequisites
Ensure you have the following packages installed:
* numpy
* opencv-python
* matplotlib

### Set up
1. Clone the repository
```bash
git clone https://github.com/K1n031/Depth_Image_Estimation_Project
cd Depth_Image_Estimation_Project
```
2. Download the dataset
Use the provided commands to download and unzip the datasets used for depth estimation.
```bash
!gdown 14gf8bcym_lTcvjZQmg8kwq3aXkENBxMQ
!unzip tsukuba.zip

!gdown 1wxmiUdqMciuTOs0ouKEISl8-iTVXdOWn
!unzip Aloe_images.zip
```

## Usage
1. Prepare dataset
Ensure that the downloaded images are extracted and organized properly.
```bash
data/
├── tsukuba/
│   ├── left.png
│   ├── right.png
│   └── groundtruth.png
├── aloe/
│   ├── left.png
│   ├── right.png
│   └── groundtruth.png
```
2. Run the project
Open the Jupyter notebook and execute the cells step by step to download datasets, process the images, estimate depth, and visualize the results.
```bash
jupyter notebook Depth_Image_Estimation_Project.ipynb
```

## Project Structure
* `Depth_Image_Estimation_Project.ipynb`: The main notebook containing the code and explanations.
* `data/`: Directory where the image dataset is stored after extraction.

## Methodology
### 1. Dataset Download
The project downloads the Tsukuba and Aloe datasets, which consist of stereo image pairs and ground truth depth maps.
### 2. Pixel-wise Matching
Pixel-by-pixel comparison between left and right images is performed to estimate depth. This technique identifies corresponding pixels in the stereo pair to calculate disparities.
### 3. Window-based Matching
Blocks of pixels (windows) are compared instead of individual pixels, which helps in reducing noise and improving depth estimation accuracy in textured regions.
### 4. Depth Map Visualization
The depth maps generated from the matching algorithms are visualized, showing the estimated depth of objects in the scene.

## Results
The system successfully generates depth maps from stereo image pairs. The results showcase the depth estimation capabilities of the algorithms, with clear disparity information observed between objects at different distances from the camera.
