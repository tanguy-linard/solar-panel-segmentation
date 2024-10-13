# Solar Panel Detection on Satellite Images

## Project Overview

This project focuses on detecting solar panels in satellite images using deep learning techniques, specifically convolutional neural networks (CNNs). The objective is to accurately identify and mark the pixels corresponding to solar panels in the imagery.

## Dataset

- **Source**: The dataset consists of 744 pairs of satellite images and their respective masks, which highlight the pixels representing solar panels. The dataset is publicly available [here](https://github.com/saizk/Deep-Learning-for-Solar-Panel-Recognition).
- **Splitting**: The dataset is split into two groups:
  - **Training set**: 90% of the images are used for training the model.
  - **Test set**: The remaining 10% are used for evaluating model performance.

## Image Import and Preprocessing

The images are imported and preprocessed before feeding them into the model. The preprocessing steps include:

- Normalization of pixel values between 0 and 1.
- Data augmentation techniques to increase the variability of the dataset and enhance the model's generalization capability.

## Model Architecture

The model is built using convolutional layers, where:

- A series of convolutional operations is applied to extract features.
- The filter weights (kernels) are learned during the training process.
- The architecture consists of encoding and decoding stages:
  - **Encoding**: Two convolutional operations reduce the image size.
  - **Decoding**: Two more convolutional operations restore the image to its original size.

## Training

The model is trained using pairs of images and their corresponding masks. The training process involves:

- Adjusting the filter weights based on the loss function.
- Repeating the process for 10 epochs.

## Predictions

The model generates a matrix where each pixel has a value between 0 and 1, representing the probability of it being part of a solar panel. The predictions undergo binarization using a threshold value of 0.5 to classify each pixel as either a solar panel or not.

## Evaluation

The model’s output is compared against the ground truth masks to assess performance. This comparison is repeated several times to validate accuracy.

## Future Work

### Limitations

- High false positive and false negative rates.
- Imprecision around edges.
- Limited computational power resulting in long training times.

### Improvements

- Use of a larger dataset for better training outcomes.
- Modifying the model architecture for increased accuracy.
- Tuning hyperparameters to optimize model performance.

## References

- Artacho, B., & Savakis, A. (2019). Waterfall Atrous Spatial Pooling Architecture for Efficient Semantic Segmentation. Sensors, 24, 5361. https://doi.org/10.3390/s19245361
- Bagwari, N., Kumar, S., & Verma, V. S. (2023). A Comprehensive Review on Segmentation Techniques for Satellite Images. Archives of Computational Methods in Engineering, 30(7), 4325‑4358. https://doi.org/10.1007/s11831-023-09939-4
- Chuang, Y., Zhang, S., & Zhao, X. (2023). Deep learning‐based panoptic segmentation : Recent advances and perspectives. IET Image Processing, 17, n/a-n/a. https://doi.org/10.1049/ipr2.12853
- Cole, R. (2023, janvier 20). A brief introduction to satellite image segmentation with neural networks. Medium. https://medium.com/@robmarkcole/a-brief-introduction-to-satellite-image-segmentation-with-neural-networks-33ea732d5bce
- Hou, J., Ling, Y., & Yujun, L. (2021). Multi-resolution dataset for photovoltaic panel segmentation from satellite and aerial imagery (v1.0) [jeu de données]. Zenodo. https://doi.org/10.5281/zenodo.5171712
- Kadhim, M., & Abed, M. (2020). Convolutional Neural Network for Satellite Image Classification. In Studies in Computational Intelligence (p. 165‑178). https://doi.org/10.1007/978-3-030-14132-5_13
- Kashyap, G. (2021, septembre 21). How to use Conv2d layers as fully connected layers. Medium. https://medium.com/@knighthawkk/how-to-use-conv2d-layers-as-fully-connected-layers-b0a82eb8a408
- Thevenot, A. (2022, février 17). Conv2d : Finally Understand What Happens in the Forward Pass. Medium. https://towardsdatascience.com/conv2d-to-finally-understand-what-happens-in-the-forward-pass-1bbaafb0b148
- Wu, A. N., & Biljecki, F. (2021). Roofpedia : Automatic mapping of green and solar roofs for an open roofscape registry and evaluation of urban sustainability. Landscape and Urban Planning, 214, 104167. https://doi.org/10.1016/j.landurbplan.2021.104167
