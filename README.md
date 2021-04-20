# Pothole Detection Application and Research Paper


## Overview

We propose an efficient and easily scalable approach for the **detection and mapping** of potholes. It as a **Deep Learning** based **two-fold** detection system that uses the **Camera, and, the Accelerometer and Gyroscope** sensors present in our Smartphones. The aim of this project is to **mitigate** the financial and human **losses** incurred every year from accidents caused by potholes by mapping the same and **informing the right authorities**.

[Research Paper](https://ieeexplore.ieee.org/document/9105737)

Team: 
[Aditya Khochare](https://github.com/AdityaPune), [Dheeraj Komandur](https://github.com/dheeraj-komandur), [Shebin Silvister](https://github.com/silvistershebin), [Uday More](https://github.com/udayvmore1), [Shubham Kokate](https://github.com/exalows)

## Introduction

Potholes have been prevalent in places with high population density and poor road management services. Since then, they have been responsible for a huge chunk of road accidents that take place across the globe every year. Our application with its two-fold detection systems minimizes the chances of a pothole going undetected and is easily deployable over a smartphone. 

<p align="center">
  <img src="https://github.com/AdityaPune/Pothole-Detection/blob/main/images/workflow.jpg" /> 
</p>
<p align="center">Fig. System Workflow</p>

## Implementation

The system we propose utilizes the following two methods of detection:

1. Camera based Detection

The rear camera records a continous stream and sends individual frames to a trained custom object detection model; the Single Shot Multibox detector(SSD). SSDs are designed to support devices with low computational abilities like the Smartphone but perform better than YOLO and CNN. Pothole images are recorded and labelled for the dataset and the TensorFlow object detection API is employed.

Picture here

2. Accelerometer and Gyroscope based Detection

The spikes in Accelerometer and Gyroscope readings when a vehicle passes over a pothole were recorded. We took the Root Mean Square of 10 readings for both the sensors that appeared around the instance in which we passed over a pothole and stored this in our database. These values were used to train a Artificial Neural Network. We used ReLu(Rectifie Linear Unit) as the activation function an Binary cross entropy loss function to measure the performance of our model.

## Conclusion

The deep-learning based system is integrated in and Android Application using Android Studio. It can be used by Road maintainence authorities for inspection and repair, navigation service providers to improve suggestions of the optimum route.

We participated in the **IEEE PuneCon 2019** and our paper was declared as the **Best paper** at the event. 

Event photo here
