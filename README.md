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
- Code Implementations: References to specific software implementations which provide practical insights into how these theories are applied in real-world SLAM systems.
- **Advanced Topics**:
  - Exploration of more complex SLAM error types and their Jacobians, such as line reprojection and IMU measurement errors.
  - Discussion on the implications of these errors on SLAM accuracy and performance.
