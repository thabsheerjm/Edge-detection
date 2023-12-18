# Edge Detection in Computer Vision

## Introduction 
Edge detection is the process of identifying sharp changes in image intensity to capture object boundaries. Edge detecion is the basis for object detection and image processing. 

## Methods for Edge Detection
- **Gradient-Based Methods**: Detecting edges by examining the maximum and minimum of the first derivative of the image. 
- **Second Derivative Methods**: Using the seconf derivative. eg:- Laplacian method

## Edge Detection Algorithms
- **Sobel Operator**
- **Canny Edge Detector**
- **Prewitt OPerator**
- **Laplacian of Gaussian (LoG)**
- **Roberts Cross Operator**


## Applications of Edge Detection
1. Image Segmentation
2. Object Detection
3. Feature Extraction



## Algorithms Implementation
1. Sobel Operator
- Sobel Operator is a widely used edge detection algorithm in image processing. It works by calculating the gradient of the image intensity at each pixel.
- An image can be considered as a two-dimensional function \(f(x,y) \), where the value of \( (x,y) \) represents the pixel intensity.
- **Gradient**: The gradient of \( f \) at any point is a 2D vector with components representing the derivatives in the horizontal and vertical directions   
   ![Gradient Formula](./Sobel-Operator/attachments/equations/gradient.png)
   
- **Sobel Kernels**: Sobel operator uses two 3x3 convolution kernels to approximate the derivatives
   Horizontal changes (Gx): ![Gx](./Sobel-Operator/attachments/equations/Gx.png)
   vertical changes (Gy): ![Gy](./Sobel-Operator/attachments/equations/Gy.png)

- **convolution**: The sobel kernels Gx  and Gy are convolved seperately with the image to produce two derivative apprximations, one for the horizontal direction and one for the vertical
    Convolution operation: ![Convolution](./Sobel-Operator/attachments/equations/convolution.png)

- **Gradient Magnitude**: The magnitude of the gradient at each pixel gives the edge stength. 
    Magnitude: ![Magnitude](./Sobel-Operator/attachments/equations/magnitude.png)

- **Gradient Direction**: The direction of the edge can be calculated as the inverse tangent of the ratio of the vertical to the horizontal gradient
     Direction: ![Direction](./Sobel-Operator/attachments/equations/direction.png)
