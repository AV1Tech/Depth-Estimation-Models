# Depth Estimation Models

Depth estimation is a crucial task in computer vision, involving the prediction of the distance of objects in a scene from the camera. This task is fundamental for various applications such as autonomous driving, robotics, and 3D scene reconstruction.

## How Depth Estimation Models Work

Depth estimation models typically work by analyzing the disparity between images captured from different viewpoints (stereo vision) or by interpreting depth cues from a single image (monocular vision). These models can be broadly categorized into two types: stereo depth estimation and monocular depth estimation.

### Stereo Depth Estimation

Stereo depth estimation involves using two or more images captured from different viewpoints. The core idea is to compute the disparity map, which is the pixel-wise difference between the corresponding points in the images. This disparity is then used to calculate the depth map using triangulation.

Key steps:
1. **Image Rectification**: Aligning the stereo images to simplify the correspondence search.
2. **Disparity Calculation**: Finding corresponding points in the rectified images and computing the disparity.
3. **Depth Calculation**: Converting the disparity map to a depth map using the known baseline distance between the cameras and the camera's focal length.

### Monocular Depth Estimation

Monocular depth estimation involves predicting depth from a single image. This task is more challenging than stereo estimation because it lacks explicit geometric information. Models typically rely on learning depth cues from large datasets through deep learning.

Key steps:
1. **Feature Extraction**: Using convolutional neural networks (CNNs) to extract features from the input image.
2. **Depth Prediction**: Employing various network architectures to predict the depth map from the extracted features.

## State-of-the-Art (SOTA) Examples of Depth Estimation Models

### DPT (Dense Prediction Transformer)

DPT leverages transformer architectures, which have shown remarkable success in natural language processing, to improve depth prediction accuracy. It uses vision transformers to capture global context and long-range dependencies.

**Key Contributions:**
- Utilizes vision transformers for dense prediction tasks.
- Achieves high accuracy by capturing global context.

**References:**
- Ranftl, R., Bochkovskiy, A., & Koltun, V. (2021). Vision Transformers for Dense Prediction. arXiv preprint arXiv:2103.13413.

### MiDaS (Mixed Depth and Scale)

MiDaS is designed to work well across diverse datasets and tasks by leveraging a mixture of depth estimation datasets during training. It uses a ResNeXt-based encoder and a decoder to produce high-quality depth maps.

**Key Contributions:**
- Combines multiple datasets for training to improve generalization.
- Uses a ResNeXt encoder for robust feature extraction.

**References:**
- Ranftl, R., Bochkovskiy, A., & Koltun, V. (2020). Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-Shot Cross-Dataset Transfer. arXiv preprint arXiv:1907.01341.

### Monodepth2

Monodepth2 focuses on improving the accuracy and robustness of self-supervised monocular depth estimation. It introduces a novel training strategy that includes a multi-scale approach and an improved photometric loss function.

**Key Contributions:**
- Self-supervised learning framework.
- Multi-scale approach for better depth estimation.

**References:**
- Godard, C., Aodha, O. M., Firman, M., & Brostow, G. J. (2019). Digging into Self-Supervised Monocular Depth Estimation. Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV).

### BTS (Boosting Monocular Depth Estimation with Skip Connections)

BTS utilizes skip connections and local planar guidance layers to enhance depth estimation accuracy. This model emphasizes the use of high-resolution features and detailed local depth patterns.

**Key Contributions:**
- Skip connections for better feature propagation.
- Local planar guidance layers for detailed depth prediction.

**References:**
- Lee, J., Han, M., Ko, D., & Suh, I. H. (2019). From Big to Small: Multi-Scale Local Planar Guidance for Monocular Depth Estimation. arXiv preprint arXiv:1907.10326.

### PSMNet (Pyramid Stereo Matching Network)

PSMNet is a stereo depth estimation model that uses spatial pyramid pooling and 3D convolutional layers to aggregate context information at multiple scales, producing high-quality disparity maps.

**Key Contributions:**
- Spatial pyramid pooling for multi-scale context aggregation.
- 3D convolutional layers for accurate disparity estimation.

**References:**
- Chang, J.-R., & Chen, Y.-S. (2018). Pyramid Stereo Matching Network. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR).

## Conclusion

Depth estimation models play a vital role in understanding and reconstructing 3D scenes. With the advancements in deep learning, state-of-the-art models have achieved remarkable accuracy and robustness, enabling their application in various fields. Models like DPT, MiDaS, Monodepth2, BTS, and PSMNet represent significant milestones in the evolution of depth estimation techniques.

## References
- Ranftl, R., Bochkovskiy, A., & Koltun, V. (2021). Vision Transformers for Dense Prediction. arXiv preprint arXiv:2103.13413.
- Ranftl, R., Bochkovskiy, A., & Koltun, V. (2020). Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-Shot Cross-Dataset Transfer. arXiv preprint arXiv:1907.01341.
- Godard, C., Aodha, O. M., Firman, M., & Brostow, G. J. (2019). Digging into Self-Supervised Monocular Depth Estimation. Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV).
- Lee, J., Han, M., Ko, D., & Suh, I. H. (2019). From Big to Small: Multi-Scale Local Planar Guidance for Monocular Depth Estimation. arXiv preprint arXiv:1907.10326.
- Chang, J.-R., & Chen, Y.-S. (2018). Pyramid Stereo Matching Network. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR).
```
