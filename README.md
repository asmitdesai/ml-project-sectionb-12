# EEG Motor Imagery Classification Project

This project implements and evaluates several machine learning pipelines to classify motor imagery tasks (left vs. right hand) from EEG recordings, as part of the UE23CS352A Machine Learning mini-project.

## Overview

The goal of this project is to build a model that can accurately distinguish between brain signals generated while imagining left-hand movement versus right-hand movement. We use the BCI Competition IV, Dataset 2a, which is a standard benchmark for this type of task.

The project involves a full machine learning workflow:
1.  **Data Preprocessing:** Loading raw EEG data, applying a standard electrode montage, filtering out noise, and segmenting the data into trials (epochs).
2.  **Feature Extraction:** Evaluating two different methods to extract meaningful features from the EEG signals: **Common Spatial Pattern (CSP)** and **Power Spectral Density (Band Power)**.
3.  **Model Training & Evaluation:** Training and comparing three different classifiers (**LDA, SVM, and k-NN**) on both sets of features to identify the best-performing combination.

## Final Result

Our analysis showed that the combination of **Common Spatial Pattern (CSP)** for feature extraction and **Linear Discriminant Analysis (LDA)** for classification yielded the best performance, achieving a final accuracy of **83.33%** on the test set.

---

## Setup and Usage

### Prerequisites

* Python 3.8+
* Anaconda (recommended)

### Installation

1.  Clone this repository to your local machine:
    ```bash
    git clone <your-github-repo-link>
    cd <your-project-folder>
    ```

2.  Install the required dependencies using pip:
    ```bash
    pip install mne scikit-learn numpy seaborn matplotlib
    ```

### How to Run

1.  Ensure the data file `A01T.gdf` is located in the root directory of the project.
2.  Launch Jupyter Notebook from your terminal:
    ```bash
    jupyter notebook
    ```
3.  Open the `Brain_Activity.ipynb` notebook and run all the cells sequentially from top to bottom to replicate the analysis and results.
