# Image Segmentation using Otsu's Method
This code implements Otsu's Method for Image Segmentation described in this paper: https://ieeexplore.ieee.org/document/4310076. The goal of this code is to calculate the threshold in the image gray scale that maximizes the difference between the object and the background, or in other words, that will separate the object from the background.

## Dataset
The dataset used to test the implementation of this method is the MNIST dataset, available as part of the torchvision library. More information on the dataset can be found here: https://yann.lecun.com/exdb/mnist/

## Implementation
The code calculates the max between class variace $\sigma_{B}^2$ among all gray scale levels k and uses that to segment the image. The formula used for between class variace $\sigma_{B}^2$ is:

$$\sigma_{B}^2 \(k \) = \frac {\[\mu_T \omega\(k\) - \mu\(k\) \]^2} {\omega\(k\) \[ 1 - \omega\(k\) \]}$$

where:

k: gray scale level.

$\omega\(k\)$: Probability of k gray scale levels from 1 to k.

$\mu_k$: Mean gray level up to k level

$\mu_T$: Total mean gray level of the original picture

## Results
