This is my SLAM-related note archive. The notes are written in English. Feel free to ask a question while reading, or see [my blog](https://alida.tistory.com) for more details.


## Notes on Various Errors and Jacobian Derivation for SLAM 
This note discusses key concepts and detailed calculations relevant to Simultaneous Localization and Mapping (SLAM), focusing on error analysis and Jacobian matrices. Here's a structured summary of its contents:
- **Introduction and Definitions**: The document introduces various errors used in SLAM such as reprojection error, photometric error, relative pose error, and line reprojection error, alongside their mathematical formulations.
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

- **Introduction and Group Theory:** The document begins by introducing basic group theory concepts, including the characteristics of groups such as associativity, identity, and inversion. It emphasizes Lie groups with a focus on their structure as smooth manifolds, meaning they can be continuously and differentiably transformed.
- **Lie Groups and Algebra**: It discusses specific properties and operations within the Lie groups SO(3) and SE(3), which represent rotations and rigid body motions in three-dimensional space, respectively. The document explains how elements like the exponential and logarithm mappings provide connections between Lie algebra and Lie groups, facilitating operations and transformations in robotics applications.
- **Applications in Robotics:** The bulk of the text explains how these mathematical structures apply to robotics, particularly in algorithms like the Extended Kalman Filter (EKF) and SLAM. It outlines how Lie groups help manage and optimize the representation of 3D object rotations and movements, contributing to more efficient and accurate computations in robotic navigation and mapping.
- Advanced Mathematical Operations: It covers more complex operations such as the Jacobian matrices in Lie groups, which are crucial for understanding how changes in one space affect another, a key component in robotic control systems.
- **Real-world Applications**: The document provides examples of how these theories are applied in real-world robotics, such as in pose estimation and map-based localization using EKF, where Lie groups and algebras facilitate the computation of robot positioning and orientation.

