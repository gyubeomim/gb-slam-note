This is my SLAM-related note archive. The notes are written in English. Feel free to ask a question while reading, or see [my blog](https://alida.tistory.com) for more details.

## arXiv preprint 
- [Notes on Kalman Filter (KF, EKF, ESKF, IEKF, IESKF)](https://arxiv.org/abs/2406.06427) 
- [Notes on Various Errors and Jacobian Derivation for SLAM](https://arxiv.org/abs/2406.06422) 

## Notes on Various Errors and Jacobian Derivation for SLAM 
This note discusses key concepts and detailed calculations relevant to Simultaneous Localization and Mapping (SLAM), focusing on error analysis and Jacobian matrices. Here's a structured summary of its contents:
- **Introduction and Definitions**:
  - The document introduces various errors used in SLAM such as reprojection error, photometric error, relative pose error, and line reprojection error, alongside their mathematical formulations.
- **Error and Optimization Formulation**:
  - Error is defined as the difference between observed and predicted values, fundamental in optimizing the SLAM process.
  - The document discusses error function derivation and the use of non-linear least squares for optimization.
- **Detailed Error Analysis**:
  - **Reprojection Error**: Calculation of Jacobians for camera poses and map points, including both theoretical foundations and practical implications.
  - **Photometric Error**: Focuses on the errors arising from image intensity differences, crucial for direct method-based SLAM.
- **Relative Pose Error**: Discusses the importance of this error in pose graph optimization, commonly used in loop closure scenarios.
- **Jacobian Derivations**:
  - Extensive derivations of Jacobian matrices for different SLAM components like camera pose, map points, and motion parameters.
  - Application of Lie theory to optimize rotation representations and transformations, enhancing computational efficiency.
- **Code Implementations**: References to specific software implementations which provide practical insights into how these theories are applied in real-world SLAM systems.
- **Advanced Topics**:
  - Exploration of more complex SLAM error types and their Jacobians, such as line reprojection and IMU measurement errors.
  - Discussion on the implications of these errors on SLAM accuracy and performance.


## Notes on Kalman Filter (KF, EKF, ESKF, IEKF, IESKF)
This note deals with various Kalman Filter models including the Kalman Filter (KF), Extended Kalman Filter (EKF), Error-State Kalman Filter (ESKF), Iterated Extended Kalman Filter (IEKF), and Iterated Error-State Kalman Filter (IESKF). Here’s a structured summary:

- **Kalman Filter (KF):**
  - It operates on a linear prediction and correction framework using Gaussian distributions to estimate state variables.
  - The process involves a prediction step followed by a correction step based on sensor measurements.
- **Extended Kalman Filter (EKF):**
  - It extends the KF to handle non-linear models by linearizing around the current estimate using a first-order Taylor approximation.
  - Similar to KF, it comprises prediction and correction steps but utilizes the Jacobian matrix for non-linear transformations.
- **Error-State Kalman Filter (ESKF):**
  - The ESKF estimates the error state rather than the actual state variables. This is beneficial in scenarios where the model dynamics are well known.
  - It employs a state augmentation approach where the state estimate is corrected by an error estimate.
- **Iterated Extended Kalman Filter (IEKF):**
  - The IEKF further extends the EKF by iterating the correction step until the changes converge to a threshold, improving the accuracy of the state estimation.
  - It recalculates the Jacobian during each iteration, adjusting the state estimates more finely.
- **Iterated Error-State Kalman Filter (IESKF):**
  - This combines the iterative approach of IEKF with the error state concept of ESKF.
  - It focuses on refining the error estimates iteratively, which can lead to more precise state estimates in complex dynamic systems.
 

## Notes on Lie Theory (SO3, SE3)
This note deals with the mathematical concepts related to Lie theory, primarily focusing on applications within robotics and computer vision for tasks such as SLAM (Simultaneous Localization and Mapping). Here’s a structured summary:
Most of the content is written referring to Joan Solà's **Lie theory for the roboticist** YouTube video.

- **Introduction and Group Theory:**
  - The document begins by introducing basic group theory concepts, including the characteristics of groups such as associativity, identity, and inversion. It emphasizes Lie groups with a focus on their structure as smooth manifolds, meaning they can be continuously and differentiably transformed.
- **Lie Groups and Algebra**:
  - It discusses specific properties and operations within the Lie groups SO(3) and SE(3), which represent rotations and rigid body motions in three-dimensional space, respectively. The document explains how elements like the exponential and logarithm mappings provide connections between Lie algebra and Lie groups, facilitating operations and transformations in robotics applications.
- **Applications in Robotics:**
  - The bulk of the text explains how these mathematical structures apply to robotics, particularly in algorithms like the Extended Kalman Filter (EKF) and SLAM. It outlines how Lie groups help manage and optimize the representation of 3D object rotations and movements, contributing to more efficient and accurate computations in robotic navigation and mapping.
- **Advanced Mathematical Operations**:
  - It covers more complex operations such as the Jacobian matrices in Lie groups, which are crucial for understanding how changes in one space affect another, a key component in robotic control systems.
- **Real-world Applications**:
  - The document provides examples of how these theories are applied in real-world robotics, such as in pose estimation and map-based localization using EKF, where Lie groups and algebras facilitate the computation of robot positioning and orientation.



## Notes on Multiple View Geometry in Computer Vision
This note is modular summary of the contents covered the book "Multiple View Geometry in Computer Vision" by Hartley and Zisserman.

- **Projective Space and Geometry**:
  - Concepts of projective space and transformations in 2D, including homogeneous representations for points and lines, degrees of freedom, intersections of lines, and ideal points at infinity.
- **Conics and Dual Conics**:
  - Detailed discussion on conics, tangent lines to conics, and the properties of dual conics which include their representation and the conditions for a line to be tangent to a conic.
- **Projective Transformations**:
  - Examination of various types of transformations, such as isometries, similarity transformations, affine transformations, and projective transformations, including their definitions and properties.
- **Camera Models**:
  - Introduction to finite and projective camera models, central projections, camera anatomy, and the basic pinhole model along with the transformations involved in imaging.
- **Epipolar Geometry and the Fundamental Matrix**:
  - Discussion on epipolar geometry, the fundamental matrix, and its properties, including geometric and algebraic derivations.
- **3D Reconstruction and Camera Calibration**:
  - Methods and theorems related to 3D reconstruction, including the projective reconstruction theorem and stratified reconstruction techniques, along with camera calibration techniques from single and multiple views.
- **Computation of Camera Matrix and Structure from Motion**:
  - Detailed methods for computing the camera matrix and addressing the structure from motion problems, including various algorithms and error metrics.


## Notes on Plücker Coordinates
This note deals with the Plücker Coordinates.
- **Introduction**
  - Plücker Coordinates offer a method to represent lines in 3D space using a point in six-dimensional space. This system is commonly used in computer graphics, robotics, and other technical fields.
- **How to Represent a Line in 3D Space**
  - Lines can be represented using points, direction vectors, or the intersection of planes.
- **Plücker Coordinate Representation**
  - Detailed methods for using Plücker Coordinates to define lines are discussed. This includes mathematical representations and the relationship between line elements.
- **Graßmann–Plücker Relations**
  - These relations provide a mathematical constraint necessary for the Plücker Coordinates to accurately represent lines.
- **Distance to the Origin**
  - Formulas to calculate the perpendicular distance from the origin to the line.
- **Up to Scale Uniqueness**
  - Discussion on how lines can be uniquely represented up to a scalar multiplication factor.
- **Plücker Matrix**
  - Introduction to the Plücker matrix, its properties, and its use in representing lines in various dimensions.
- **Dual Plücker Coordinate Representation**
  - A dual system of the Plücker Coordinates used for representing lines through the intersection of planes.
- **Uses**
  - Practical applications of Plücker Coordinates, including the intersection of lines, joining and meeting of lines and planes, and their uses in projective geometries.
- **Plücker Line-based Optimization**
  - How Plücker Coordinates are used in optimization algorithms and the specifics of transforming these coordinates for computational models.
- **Error Function Formulation**
  - Details on how to use these coordinates in optimization problems, including the calculation of reprojection errors and adjustments using Jacobian matrices.
