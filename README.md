# Surface-Crack-Detection-with-DL
This is a Surface Crack Detection project implemented with the Tensorflow. We fine tuning some deep learning models (like VGG 19, VGG16, MobileNetV2, ...). Use Surface Crack Detection dataset available on kaggle.
## Context
Concrete surface cracks are major defect in civil structures. Building Inspection which is done for the evaluation of rigidity and tensile strength of the building. Crack detection plays a major role in the building inspection, finding the cracks and determining the building health.
## Dataset
The datasets contains images of various concrete surfaces with and without crack. The image data are divided into two as negative (without crack) and positive (with crack) in separate folder for image classification. Each class has 20000images with a total of 40000 images with 227 x 227 pixels with RGB channels. The dataset is generated from 458 high-resolution images (4032x3024 pixel) with the method proposed by Zhang et al (2016). High resolution images found out to have high variance in terms of surface finish and illumination condition. No data augmentation in terms of random rotation or flipping or tilting is applied.

This dataset is taken from the website Mendeley Data - Crack Detection, contributed by Çağlar Fırat Özgenel.

> Özgenel, Çağlar Fırat (2019), “Concrete Crack Images for Classification”, Mendeley Data, v2
http://dx.doi.org/10.17632/5y9wdsg2zt.2

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/data1.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/data1.png" align="center"></a>
</p>

### Number of samples

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/np.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/np.png" align="center"></a>
</p>

### Examples of Prediction

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/predict2.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/predict2.png" align="center"></a>
</p>

## MobileNetV2 architecture
MobileNetV2 is a convolutional neural network architecture that seeks to perform well on mobile devices. It is based on an inverted residual structure where the residual connections are between the bottleneck layers.

<p align="center">
<a href="https://production-media.paperswithcode.com/methods/Screen_Shot_2020-06-06_at_10.37.14_PM.png"><img src="https://production-media.paperswithcode.com/methods/Screen_Shot_2020-06-06_at_10.37.14_PM.png" align="center" width="400" height="400" ></a>
</p>

### Results

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion2.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion2.png" align="center"></a>
</p>


|               | precision     |recall  |f1-score |support|
| ------------- |:-------------:| :-----: |:-----:   |-----:   |
|  NEGATIVE     | 1.00          | 1.00   |  1.00   |  6082 |
| POSITIVE      | 1.00          |  1.00  |  1.00   |    5918   |
| accuracy      | 1.00          |  1.00  |  1.00     |    12000   |

Test Loss| Test Accuracy
--- | ---
0.04124 | 99.83%

## VGG16 architecture
VGG16 is a convolution neural net (CNN ) architecture which was used to win ILSVR(Imagenet) competition in 2014. It is considered to be one of the excellent vision model architecture till date. The 16 in VGG16 refers to it has 16 layers that have weights. This network is a pretty large network and it has about 138 million (approx) parameters.

<p align="center">
<a href="https://miro.medium.com/max/940/1*3-TqqkRQ4rWLOMX-gvkYwA.png"><img src="https://miro.medium.com/max/940/1*3-TqqkRQ4rWLOMX-gvkYwA.png" align="center" ></a>
</p>

### Results

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion3.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion3.png" align="center"></a>
</p>


|               | precision     |recall  |f1-score |support|
| ------------- |:-------------:| :-----: |:-----:   |-----:   |
|  NEGATIVE     | 1.00          | 1.00   |  1.00   |  6082 |
| POSITIVE      | 1.00          |  1.00  |  1.00   |    5918   |
| accuracy      | 1.00          |  1.00  |  1.00     |    12000   |

Test Loss| Test Accuracy
--- | ---
0.00840 | 99.77%

## DenseNet-121 architecture
DenseNet (Dense Convolutional Network) is an architecture that focuses on making the deep learning networks go even deeper, but at the same time making them more efficient to train, by using shorter connections between the layers. DenseNet-121 has 120 Convolutions and 4 AvgPool. All layers i.e. those within the same dense block and transition layers, spread their weights over multiple inputs which allows deeper layers to use features extracted early on.

<p align="center">
<a href="https://www.researchgate.net/profile/Noha-Radwan-3/publication/334170752/figure/fig5/AS:776225345785857@1562077952441/A-schematic-illustration-of-the-DenseNet-121-architecture-82.png"><img src="https://www.researchgate.net/profile/Noha-Radwan-3/publication/334170752/figure/fig5/AS:776225345785857@1562077952441/A-schematic-illustration-of-the-DenseNet-121-architecture-82.png" align="center" width="520" ></a>
</p>
 
### Results

<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion4.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion4.png" align="center"></a>
</p>


|               | precision     |recall  |f1-score |support|
| ------------- |:-------------:| :-----: |:-----:   |-----:   |
|  NEGATIVE     | 1.00          | 1.00   |  1.00   |  6082 |
| POSITIVE      | 1.00          |  1.00  |  1.00   |    5918   |
| accuracy      | 1.00          |  1.00  |  1.00     |    12000   |

Test Loss| Test Accuracy
--- | ---
0.01813 | 99.52%

## VGG19 architecture
VGG-19 architecture is very much similar to VGG-16. We have 3 additional convolutional layers for the VGG-16 network.
<p align="center">
<a href="https://www.researchgate.net/profile/Clifford-Yang/publication/325137356/figure/fig2/AS:670371271413777@1536840374533/llustration-of-the-network-architecture-of-VGG-19-model-conv-means-convolution-FC-means.jpg"><img src="https://www.researchgate.net/profile/Clifford-Yang/publication/325137356/figure/fig2/AS:670371271413777@1536840374533/llustration-of-the-network-architecture-of-VGG-19-model-conv-means-convolution-FC-means.jpg" align="center" ></a>
</p>

### Results
<p align="center">
<a href="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion5.png"><img src="https://github.com/mo26-web/Surface-Crack-Detection-with-DL/blob/main/images/confusion5.png" align="center"></a>
</p>


|               | precision     |recall  |f1-score |support|
| ------------- |:-------------:| :-----: |:-----:   |-----:   |
|  NEGATIVE     | 1.00          | 1.00   |  1.00   |  6082 |
| POSITIVE      | 1.00          |  1.00  |  1.00   |    5918   |
| accuracy      | 1.00          |  1.00  |  1.00     |    12000   |

Test Loss| Test Accuracy
--- | ---
0.01353 | 99.63%
