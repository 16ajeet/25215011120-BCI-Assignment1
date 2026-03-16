# Brain Wearable Monitoring Dataset – Exploratory Data Analysis (EDA)

## Overview

This project performs an exploratory data analysis (EDA) on the **Brain Wearable Monitoring Dataset** available on PhysioNet.

The dataset contains **multimodal physiological signals collected from wearable devices** during cognitive experiments involving auditory, gustatory, and olfactory stimulation. The objective of this analysis is to explore the dataset structure, extract key metadata, and visualize physiological signals to better understand patterns in cognitive state monitoring.

Dataset Source:
https://physionet.org/content/brain-wearable-monitoring/1.0.0/

---

# Objectives

The main goals of this project are:

* Understand the structure of the Brain Wearable Monitoring dataset.
* Extract important dataset metadata such as participants, sessions, and signal types.
* Perform exploratory data analysis on physiological signals.
* Visualize signal behavior and relationships between variables.
* Generate a structured dataset summary table.

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

# Key Outcome

This project provides:

* a structured overview of the Brain Wearable Monitoring dataset
* exploratory analysis of physiological signals
* visual insights into wearable cognitive monitoring data
* an automatically generated dataset summary

The analysis serves as a foundation for further research tasks such as **cognitive state classification, stress detection, and wearable health monitoring applications**.

---

# License

Dataset provided by PhysioNet. Please refer to the dataset page for usage guidelines and citation requirements.
