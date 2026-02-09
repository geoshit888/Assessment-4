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

Before we can classify the data, we must correct it for things like the satellite’s exact position. Once the data is cleaned and aligned, we use Gaussian Mixture Models (GMM) to group the waveforms into sea ice and leads. We then compare our results to ESA’s ground truth to make sure our AI is accurate.
