---
title: "AI Transformers for Diagnosis of Cardiac Diseases"
collection: projects
type: "Medical Image Processing"
permalink: /projects/Cardio-Net-Neural-Network-based-Diagnosis-of-Cardiac-Diseases
venue: "An AI-cardiology project collaborated with Stanford Engineering and Stanford Medicine"
date: 2023-01-25
location: "USTC Hefei, China"
---

Participated in the project as a short-term Research Assistant (RA)*(February 2023 - March 2023)*.

# Motivation

* Cardiovascular diseases (CVDs) remain one of the leading causes of morbidity and mortality worldwide, underscoring the critical need for accurate and timely diagnosis. Traditional methods for diagnosing heart conditions often rely on the expertise of human physicians, who analyze complex data such as Cardiovascular Magnetic Resonance (CMR) images. However, this approach is constrained by factors like human error, subjectivity, and the shortage of specialized medical professionals, which can impede early detection and treatment.
* To address these challenges, our project aims to leverage the power of deep neural networks to revolutionize the process of heart disease screening and diagnosis. By harnessing the advancements in computer vision and machine learning, we seek to create an automated system capable of analyzing CMR images and accurately detecting the presence of heart diseases, as well as identifying the specific type of cardiovascular condition. This innovation holds the potential to significantly enhance the efficiency and accuracy of diagnostic procedures, enabling earlier intervention and thereby improving patient outcomes.

# Method

* We convert various modalities of CMR data into images/videos as the output of the network.
* We have built two models for automated cardiac disease diagnosis, with CNN-LSTM serving as the baseline and VST achieving the best performance on this task.
* We have proposed a working mechanism: firstly, screening cardiac health based on cine-mode CMR data; if an unhealthy condition is determined, then introducing LGE-mode CMR data to further diagnose the type of disease.

# Personal Achievement
* Assist in building the dataset: Utilize ITK-SNAP to segment the magnetic resonance data, extract ROIs, and ultimately convert them into image format.
* Utilize the NNI(Neural Network Intelligence) library to select the optimal hyperparameter settings for the CNN-LSTM model.
* Raise the F1-score of the CNN-LSTM model from 0.89 to 0.91 by incorporating weighted sampling.
