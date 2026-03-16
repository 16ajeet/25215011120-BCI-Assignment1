# ============ ASSIGNMENT 1 ==============

# Submitted By- 
Name - Ajeet Kumar

Branch - AI

Scholar Number - 25215011120

Subject - BCI

# Files
1. Kaggle Notebook with visualizations
2. Summary in csv file
3. Readme

# Brain Wearable Monitoring Dataset – Exploratory Data Analysis (EDA)

## Overview

This project performs an exploratory data analysis (EDA) on the **Brain Wearable Monitoring Dataset** available on PhysioNet.

The dataset contains **multimodal physiological signals collected from wearable devices** during cognitive experiments involving auditory, gustatory, and olfactory stimulation. The objective of this analysis is to explore the dataset structure, extract key metadata, and visualize physiological signals to better understand patterns in cognitive state monitoring.

Dataset Source:
https://physionet.org/content/brain-wearable-monitoring/1.0.0/

---

# Objectives

The main goals of this project are:

* no. of participants
* sampling frequency
* No. of experiments
* trails, sessions
* no. of classes
* duration of recording
* event markers

Note:- These data alongwith some essential EDA have been shown in kaggle notebook and the csv file contains all the necessary summary generated to get complete understanding of dataset.

---

# Dataset Description

The dataset contains physiological signals collected using wearable devices during cognitive tasks. The experiments investigate how different sensory stimuli affect cognitive states.

Signals included in the dataset:

* EEG (Electroencephalography)
* EDA (Electrodermal Activity)
* BVP (Blood Volume Pulse)
* Skin Temperature
* Accelerometer data

These signals are recorded while participants perform **working memory tasks (n-back tasks)** under different experimental conditions.

---

# Analysis Workflow

## 1. Dataset Download

The dataset was downloaded from PhysioNet using the following command:

```
wget -r -N -c -np https://physionet.org/files/brain-wearable-monitoring/1.0.0/
```

This command recursively downloads the complete dataset.

---

## 2. Dataset Structure Inspection

The folder structure was explored to identify:

* participant folders
* experiment sessions
* physiological signal files
* event marker files

Understanding the dataset hierarchy is essential before performing analysis.

---

## 3. Metadata Extraction

A Python script was used to automatically extract key dataset statistics including:

* number of participants
* number of sessions
* available signal types
* total number of files

This metadata was later used to generate the dataset summary.

---

## 4. Data Loading

Signal files were loaded using **Pandas**. Each physiological signal is stored as a CSV file containing time-series measurements.

Example signals analyzed:

* Electrodermal Activity (EDA)
* Blood Volume Pulse (BVP)
* Skin Temperature
* Accelerometer signals
* EEG signals

---

## 5. Data Exploration

Several exploratory analysis techniques were applied:

* Statistical summary of signals
* Missing value analysis
* Signal distribution analysis
* Time-series visualization
* Correlation analysis between physiological signals
* Outlier detection using boxplots

These analyses help reveal patterns and relationships in physiological data.

---

## 6. Recording Duration Estimation

Recording duration was estimated using the formula:

duration = number_of_samples / sampling_frequency

Typical sampling frequencies used in the dataset include:

* EDA – 4 Hz
* BVP – 64 Hz
* Temperature – 4 Hz
* Accelerometer – 32 Hz
* EEG – ~256 Hz

---

## 7. Dataset Summary Generation

A dataset summary table was generated containing key dataset properties such as:

* number of participants
* number of experiments
* number of sessions
* signal types
* sampling frequencies
* event markers
* estimated recording duration

The generated summary is stored in:

dataset_summary.csv

---

# Repository Contents

This repository intentionally maintains a minimal structure for clarity.

```
brain_wearable_EDA.ipynb
dataset_summary.csv
README.md
```

### brain_wearable_EDA.ipynb

Kaggle notebook containing the full exploratory data analysis workflow.

### dataset_summary.csv

Automatically generated dataset metadata summary.

### README.md

Documentation explaining the analysis process.

---

# Tools and Technologies

The analysis was performed using the following tools:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Kaggle Notebook Environment

---

# License

Dataset provided by PhysioNet. Please refer to the dataset page for usage guidelines and citation requirements.
