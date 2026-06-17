# Introduction

viewephys is a lightweight Python viewer for electrophysiology data. Developed by the International Brain Laboratory (IBL), it provides a fast and interactive way to visualize recordings without extensive preprocessing or setup. 

Designed for neuroscientists, electrophysiologists, and developers working with neural recordings, it supports common tasks such as checking signal quality, navigating across channels and time, monitoring experiments in progress, and quickly assessing newly acquired data.

Unlike analysis packages that focus on spike sorting or downstream processing, viewephys is primarily a visualization tool. Its purpose is to provide a direct view of the underlying signals, helping users understand their recordings and identify potential issues before further analysis.

## What Can I Use viewephys For?

Electrophysiology recordings can be challenging to inspect directly. Datasets are often large, contain hundreds of channels, and may require significant processing before they can be visualized. When working with raw recordings, it is often useful to quickly assess data quality before beginning downstream analysis.

Common uses for viewephys include:

1. Inspect existing recordings – Open previously acquired data to assess signal quality, investigate artifacts, and explore recordings across channels and time.
2. Monitor live acquisitions – Visualize data as it is being recorded to quickly identify potential issues during an experiment.
3. Visualize data from Python – Display recordings, NumPy arrays, or processed signals directly from a Python session. 

For step-by-step examples of these workflows, see the [Quickstart](quickstart) and [Python API](python-api) sections.

By providing fast, interactive access to the underlying signals, viewephys makes it easy to understand what was recorded and identify potential issues early in the analysis workflow.

## Supported Input Data 

viewephys is designed to visualize a wide range of electrophysiology recordings and is not restricted to a specific acquisition system. It primarily works with binary (.bin) electrophysiology recordings and is commonly used with Neuropixels data. It can also visualize data stored as NumPy arrays, allowing both raw and processed signals to be inspected through the [Python API](python-api). 

> **Note:** When available, viewephys uses SpikeGLX metadata (.meta) files to determine recording information such as channel count and sampling rate. If no metadata file is present, these parameters can be specified manually when loading data through the Python API (see Loading NumPy Arrays).

**Documentation Overview**

This documentation covers:

- [Installation](installation) of viewephys 
- [Quickstart](quickstart) 
- [GUI navigation and display options](gui)
- [Python API](python-api) usage
- Usage Examples 
- [Troubleshooting](troubleshooting) common issues

