# Introduction

viewephys is a lightweight Python viewer for electrophysiology data. Developed by the International Brain Laboratory (IBL), it provides a fast and interactive way to visualize recordings without extensive preprocessing or setup.

Designed for neuroscientists, electrophysiologists, and developers working with neural recordings, it supports common tasks such as checking signal quality, navigating across channels and time, monitoring experiments in progress, and quickly assessing newly acquired data.

Unlike analysis packages that focus on spike sorting or downstream processing, viewephys is primarily a visualization tool. Its purpose is to provide a direct view of the underlying signals, helping users understand their recordings and identify potential issues before further analysis.

Use Cases

Electrophysiology recordings can be challenging to inspect directly. Datasets are often large, contain hundreds of channels, and may require significant processing before they can be visualized. When working with raw recordings, it is often useful to quickly assess data quality before beginning downstream analysis.

Common uses for viewephys include:

* Checking signal quality immediately after a recording
* Browsing recordings across channels and time
* Monitoring data during acquisition
* Investigating artifacts or noisy channels
* Visualizing data directly from a Python session

By providing fast, interactive access to the underlying signals, viewephys makes it easy to understand what was recorded and identify potential issues early in the analysis workflow.

**Key Features**

viewephys supports several common workflows:

- Open and inspect previously acquired recordings
- Monitor recordings during data acquisition
- Visualize NumPy arrays and processed data from Python

**Documentation Overview**

This documentation covers:

- Installation
- Quickstart workflows
- Viewer navigation and display options
- Python API usage
- Troubleshooting common issues

