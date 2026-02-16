# Assessment-4

## Getting Started
The task for GEOL0069: AI for Earth Observation 25/26 (Week 4) is to classify Sentinel-3 radar altimetry waveforms over Arctic sea ice using Gaussian Mixture Models (GMM). This unsupervised machine learning method clusters waveforms into sea ice or leads based on their reflection patterns. Results are validated against ground truth data from the European Space Agency (ESA) to quantify classification accuracy via a confusion matrix.

### Prerequisites
* To run the notebook, you must install the following Python software:
```
pip install rasterio
```
```
pip install netCDF4
```
* Mounting Google Drive on Google Colab
```
from google.colab import drive:
drive.mount('/content/drive')
```

### What is Google Colab?
Google Colab is a cloud-based service that allows you to write and execute Python code through your browser. It is particularly well-suited for AI and machine learning tasks because:

* Zero Configuration: No local environment setup is required.
* Free GPU Access: Provides high-performance hardware accelerators for intensive computations.
* Collaboration: Allows for easy sharing and real-time editing, similar to Google Docs.
* Pre-installed Libraries: Most popular data science libraries (like matplotlib) come pre-loaded.

## Context
The Sentinel-3 mission is part of the European Copernicus program, run by the European Space Agency (ESA). It uses two satellites to monitor the Earth’s oceans and ice from around 800 km above. This mission is essential for tracking how Arctic sea ice changes over time, which helps scientists understand global warming. 

The satellite uses a tool called a Radar Altimeter (SRAL). This is an active sensor that sends radar pulses down to Earth and measures the echo that bounces back. Because it uses radar rather than cameras, it can see through clouds and work during the dark polar winter. The returned signal is called a waveform, and its shape acts like a fingerprint that tells us what the radar hit. 

## Getting Started
Before we can classify the data, we must correct it for things like the satellite’s exact position. Once the data is cleaned and aligned, we use Gaussian Mixture Models (GMM) to group the waveforms into sea ice and leads. We then compare our results to ESA’s ground truth to make sure our AI is accurate.

Please check for more information about the mission: https://sentinels.copernicus.eu/copernicus/sentinel-3

## Gaussian Mixture Models
In this assignment, Gaussian Mixture Model (GMM) is used to classify Sentinel-3 radar altimetry waveforms into sea ice and leads. Gaussian Mixture Models (GMM) are an unsupervised machine learning method used to group data into different clusters. The model assumes that the data come from a mixture of several normal (Gaussian) distributions, where each distribution represents a different class within the dataset. Sea ice and leads produce different echo shapes because radar signals reflect differently from rough ice surfaces compared to smooth open water. By analysing these differences, the model can automatically separate the waveforms into two groups without needing labelled training data.

A key advantage of GMM is that it performs soft clustering. This means the model estimates the probability that each waveform belongs to each class instead of making a strict decision. This is useful for radar altimetry data because echoes from sea ice and leads can sometimes overlap and are not always clearly distinct.

The classification is based on waveform features such as backscatter strength, peakiness, and stack standard deviation. It describes how strong, sharp, and wide each echo is. After clustering, the results are compared with official surface type labels provided by the European Space Agency using a confusion matrix to evaluate the accuracy of the classification.

## Code explanation
To see how the code is implemented, please refer to the notebook: [Week4_Unit_2_Unsupervised_Learning_Methods.ipynb](Week4_Unit_2_Unsupervised_Learning_Methods.ipynb).

Within the notebook, explanations of the workflow and results are provided in bold text to help readers understand how the classification process works step by step.


