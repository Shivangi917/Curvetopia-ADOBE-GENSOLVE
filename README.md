# CURVETOPIA: A Journey into the World of Curves
Project for Adobe GenSolve Hackathon (Round 2) Hackathon

## Overview
This project addresses three critical challenges in 2D curve processing: regularization, symmetry analysis, and occlusion completion. The primary goal is to enhance and complete 2D curves by ensuring smoothness, detecting and analyzing symmetry, and effectively handling occlusions. Advanced computational geometry techniques have been employed to achieve these objectives, with solutions validated against test cases.

This project was developed using ![Python](https://img.shields.io/badge/python-3.10-blue) and executed in ![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=google-colab&logoColor=white)

## Project Structure

The project is organized into the following files and folders:

- `problems`: Folder containing the test case files
- `Curvetopia Problem Statement.pdf`: PDF file containing the problem statement for the hackathon.
- `Regularization_and_Symmetry.ipynb`: Jupyter notebook with code for regularization and symmetry analysis.
- `Curve_Completion_(Occlusion).ipynb`: Jupyter notebook with code for curve completion (occlusion handling).

## Project Components

### 1. Regularization
**Objective:** Smooth and regularize curves to ensure they appear smooth, consistent, and free from irregularities.

**Approach:**
- Regularize open curves by checking if they can be approximated as straight lines or need to be smoothed. Straight lines are detected using **linear regression**, while irregular curves are smoothed using the **Savitzky-Golay filter**.
- Regularize closed curves by adjusting points and identifying regular shapes. Shapes are classified into known categories like triangles, squares, rectangles, circles, ellipses, and stars using **contour analysis** and ellipse fitting.
  - **Geometric Shape Classification**: Identify shapes based on the number of sides, aspect ratio, and circularity.

**Significance:** Regularization is the foundation for accurate symmetry analysis, as it ensures the curves are in their most ideal form before further processing.


### 2. Symmetry Analysis
**Objective:** Detect and analyze symmetry in 2D shapes and curves, providing insights into their structural properties.

**Approach:**
-  Identify symmetry by checking for **reflective symmetry** across potential lines. Potential lines include lines formed by connecting vertices of the contour and perpendicular bisector lines.
-  Identify lines of symmetry based on the shape's geometry. For example, detected circles are shown to have radial symmetry.

**Significance:** Understanding symmetry is crucial for many applications, from computer graphics to pattern recognition. This component ensures that the inherent symmetry of each shape is accurately captured and visually represented.

### 3. Curve Completion (Handling Occlusions)
**Objective:** Handle occlusions in 2D shapes by completing curves that have gaps due to overlaps or other disruptions.

**Approach:**
- **Interpolation and Extrapolation**: Complete existing incomplete curves using spline interpolation. Use of extrapolation to extend curves when necessary.
- **Model Fitting with RANSAC**: Fit a shape model (ellipse or circle) to a set of 2D points using RANSAC. Select the model with the best fit. Improve the initial model fitted by RANSAC for better accuracy by use of optimization techniques (L-BFGS-B) to refine model parameters.

**Significance:** Occlusion is a common challenge in image processing and computer vision. Accurately completing occluded shapes is essential for applications ranging from object recognition to digital art restoration.

## Test Cases
The project has been rigorously tested using a series of test cases provided by Adobe, located in the `problems` folder. These test cases cover a wide range of scenarios, ensuring that the algorithms perform well under various conditions, including complex shapes, multiple occlusions, and varying levels of symmetry.

## Authors
- Abhisri Shaha
    - [abhisri.shaha.cse26@heritageit.edu.in](mailto:abhisri.shaha.cse26@heritageit.edu.in)
    - +91 9831319710
- Shivangi Shree
    - [shivangi.shree.cse26@heritageit.edu.in](mailto:shivangi.shree.cse26@heritageit.edu.in)
    - +91 9153899151

## Conclusion
This project demonstrates a deep understanding of computational geometry and its application to real-world problems in 2D curve processing. By addressing regularization, symmetry analysis, and curve completion, we have developed robust solutions applicable to various domains, including computer graphics, pattern recognition, and digital image processing. We are confident that our work showcases both the technical depth and practical applicability that Adobe seeks.

