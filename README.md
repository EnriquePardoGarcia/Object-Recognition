# Object Recognition with Image Masks and Data Augmentation

## Overview
This project focuses on **recognizing and classifying animal objects** in images using **pixel-level masks** and **manual data augmentation**.  
Developed as part of a Computer Vision course, it provides a reproducible pipeline for loading, preprocessing, augmenting, and analyzing images of multiple object classes.

---

## Problem Statement
Object recognition is a fundamental challenge in computer vision, requiring accurate classification of objects across complex and unbalanced datasets.  
This project addresses key issues such as:

- Limited number of images per class  
- Variations in lighting, orientation, and object scale  
- The need to apply **masks** to identify each object's region of interest (ROI)

The objective is to improve recognition performance by increasing dataset diversity through **augmentation** and by analyzing **color-based descriptors** extracted from masked regions.

---

## Methodology

### 1. Dataset Loading
Images and their corresponding masks are loaded from a structured directory.  
Each image is resized to a fixed resolution and normalized between 0 and 1.

### 2. Mask Application
Binary masks are applied to isolate each object's region of interest (ROI), ensuring that background pixels do not interfere with feature extraction.

### 3. Data Augmentation
To compensate for limited data, several manual transformations are applied:

| Transformation | Description |
|----------------|--------------|
| Horizontal & Vertical Flips | Simulate different orientations |
| Random Rotations & Shifts | Add spatial variability |
| Brightness & Contrast Adjustments | Handle lighting variations |
| Gamma Correction | Enhance visual contrast |

### 4. Feature Extraction
For each masked object, **average RGB values** and additional color descriptors are computed.  
These features are used to train classifiers or visualize the separability between object classes.

---

## Results
The **augmented dataset** increases both variability and training size, leading to improved model robustness.  
Objects are successfully identified and isolated using masks, while color-based features enable accurate differentiation between categories such as **elephant**, **rhino**, and others.

| Aspect | Improvement Observed |
|--------|----------------------|
| Dataset Size | Expanded through augmentation |
| Model Robustness | Improved against rotation and brightness changes |
| Feature Distinction | Enhanced through color-space analysis |

---

## Visualization
The project includes visualization functions to display:
- Original and augmented images  
- Binary masks and ROI extraction  
- Comparative plots of color feature distributions

Example:

```python
# Display original vs augmented samples
show_original_and_augmented(image_path, mask_path)
```

---

## Folder Structure
```
├── data/
│   ├── images/                 # Original input images
│   ├── masks/                  # Corresponding binary masks
│   ├── augmented/              # Output augmented samples
│   └── features.csv            # Extracted features (RGB, stats, etc.)
├── notebooks/
│   └── parte2_Pardo_Garcia_Enrique.ipynb
├── src/
│   └── augmentation_utils.py   # Helper functions for augmentation
├── results/
│   └── visualizations/         # Example outputs and plots
└── README.md
```

---

## Technologies Used
- **Language:** Python  
- **Libraries:** NumPy, OpenCV, Matplotlib, Scikit-image, Pandas  

---

## Execution Guide
1. Clone the repository:
   ```bash
   git clone https://github.com/EnriquePardoGarcia/computer-vision-projects.git
   cd computer-vision-projects/object-recognition
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   ```bash
   jupyter notebook parte2_Pardo_Garcia_Enrique.ipynb
   ```

4. Execute the following steps inside the notebook:
   - Load dataset and masks  
   - Apply augmentations  
   - Extract color-based features  
   - Visualize object separability

---

## Conclusion
This project demonstrates a **practical, feature-based approach to object recognition** using **masks and data augmentation**.  
It showcases how careful preprocessing and augmentation can significantly enhance recognition performance, even in small datasets, and lays the groundwork for future **deep learning extensions**.

---

## Author
Developed by **Enrique Pardo García**  
*Data Science and Engineering student – University of A Coruña*
