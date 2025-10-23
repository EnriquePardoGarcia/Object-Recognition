# Object-Recognition
Project Overview

This project aims to recognize and classify animal objects in images using pixel-level masks and manual data augmentation.
It was developed as part of a Computer Vision course and focuses on creating a reproducible pipeline for loading, processing, augmenting, and analyzing images of different object classes.

Problem Statement

Object recognition is a fundamental task in computer vision that requires distinguishing multiple classes within complex and often unbalanced datasets.
The challenges addressed in this project include:

Limited number of images per class.

Variations in lighting, orientation, and object scale.

The need to use masks to identify the region of interest (ROI) of each object.

The objective is to improve recognition performance by increasing dataset diversity through augmentation and by analyzing color-based descriptors extracted from the masked regions.

Methodology

Dataset Loading
Images and their corresponding masks are loaded from a structured directory.
Each image is resized to a fixed resolution and normalized between 0 and 1.

Mask Application
Binary masks are used to isolate the region corresponding to the object, ensuring that background pixels do not interfere with the feature extraction process.

Data Augmentation
To compensate for the small dataset size, several manual transformations are applied:

Horizontal and vertical flips

Random rotations and shifts

Brightness and contrast adjustments

Gamma correction

Feature Extraction
Average RGB values and additional descriptors are computed for each object region.
These features are later used to train simple classifiers or to visualize class separability.

Results

The augmented dataset significantly increases the variability and size of the training set, improving model robustness.
Objects are successfully identified and isolated through masks, while the color features enable accurate differentiation between classes such as elephant, rhino, and others.

Conclusion

This project demonstrates a practical approach to object recognition using masks and data augmentation.
It highlights how preprocessing and augmentation can enhance model performance even with limited data, and it establishes a foundation for future work in feature-based or deep learning object detection.

Visualization
The project includes functions to display both original and augmented images, as well as their corresponding binary masks.
