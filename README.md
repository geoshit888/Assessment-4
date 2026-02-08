# Assessment-4

## Getting Started
The task for GEOL0069: AI for Earth Observation 25/26 (Week 4) is to classify Sentinel-3 radar altimetry waveforms over Arctic sea ice using Gaussian Mixture Models (GMM). This unsupervised machine learning method clusters waveforms into sea ice or leads based on their reflection patterns. Results are validated against ground truth data from the European Space Agency (ESA) to quantify classification accuracy via a confusion matrix.

### Prerequisites
' - To run the notebook, you must install the following Python software:
```
pip install rasterio
```
```
pip install netCDF4
```
' - Mounting Google Drive on Google Colab
```
from google.colab import drive:
drive.mount('/content/drive')
```

### What is Google Colab?
Google Colab is a cloud-based service that allows you to write and execute Python code through your browser. It is particularly well-suited for AI and machine learning tasks because:

' - Zero Configuration: No local environment setup is required.
' - Free GPU/TPU Access: Provides high-performance hardware accelerators for intensive computations.
' - Collaboration: Allows for easy sharing and real-time editing, similar to Google Docs.
' - Pre-installed Libraries: Most popular data science libraries (like scikit-learn and matplotlib) come pre-loaded.
