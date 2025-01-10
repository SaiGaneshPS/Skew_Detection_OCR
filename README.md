# Skew Correction using Deep Learning

## Overview
This project aims to correct the skew in images of receipts or bills using deep learning by framing it as a classification problem. Traditional methods and current regression algorithms are limited in terms of the skew angles they can handle accurately. This project explores the capability of various state-of-the-art neural network architectures to identify and correct a wide range of skew angles.

## Objectives
1. Formulate skew correction as a classification problem.
2. Create datasets with various skew angles for training and testing.
3. Compare performance across different deep learning models.
4. Implement data augmentation and analyze its impact on performance.

## Models Compared
- DenseNet161
- MobileNet (mobilenetv3_large_100_miil_in21k)
- VGG19 (vgg19_bn)
- ConvNext (convnext_base_in22k)
- InceptionV3 (inception_v3)
- ResNet50 (resnet50)
- InceptionResNet (inception_resnet_v2)
- ResNetV2 (resnetv2_50)
- Vision Transformer (vit_base_patch16_224_in21k)
- Swin Transformer (swin_base_patch4_window7_224_in22k)

## Datasets
Datasets were created with images rotated at the following degrees: 180, 90, 30, 15, 5. Here is a summary:

| Resolution | Number of Images | Training | Validation | Testing |
|------------|------------------|----------|------------|---------|
| 180        | 2976             | 564      | 176        | 2236    |
| 90         | 5951             | 1127     | 352        | 4472    |
| 30         | 17852            | 3380     | 1056       | 13416   |
| 15         | 35703            | 6759     | 2112       | 26832   |
| 5          | 107168           | 20276    | 6336       | 80496   |

## Results
### Comparison between DenseNet and Swin Transformer

| Resolutions | Densenet | Swin Transformer |
|-------------|----------|------------------|
|             | Without Data Augmentation | With Data Augmentation | Without Data Augmentation | With Data Augmentation |
| 180         | 97% Accuracy, 97% F1 Score | 97% Accuracy, 97% F1 Score | 99% Accuracy, 99% F1 Score | 99% Accuracy, 99% F1 Score |
| 90          | 99% Accuracy, 99% F1 Score | 93% Accuracy, 93% F1 Score | 88% Accuracy, 88% F1 Score | 99% Accuracy, 99% F1 Score |
| 30          | 99% Accuracy, 99% F1 Score | 94% Accuracy, 94% F1 Score | 99% Accuracy, 99% F1 Score | 99% Accuracy, 99% F1 Score |
| 15          | 99% Accuracy, 99% F1 Score | 98% Accuracy, 98% F1 Score | 99% Accuracy, 99% F1 Score | 99% Accuracy, 99% F1 Score |
| 5           | 98% Accuracy, 98% F1 Score | 93% Accuracy, 93% F1 Score | 99% Accuracy, 99% F1 Score | 98% Accuracy, 98% F1 Score |

## Conclusion
When viewed as a classification problem, skew correction with deep learning models can perform well even in cases where traditional regression algorithms fall short. The Swin Transformer, especially with data augmentation, achieves an average accuracy of 99% across various datasets, making it highly effective for this task.

## References
- Kumar et al., 2020
- Jirasuwankul, 2011
- Bezmaternykh and Nikolaev, 2019
- Kumar et al., 2012
- Panwar et al., 2011
- Fabrizio, 2014
- Boiangiu et al., 2020

## Acknowledgements
We thank the researchers and developers whose work was referenced and built upon in this project.
