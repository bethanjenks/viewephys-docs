# Installation

This page will guide you through installing viewephys and verifying that the installation was successful.

## Requirements

Before installing viewephys, ensure you have:

- Python >= 3.10
- pip (included with most Python installations; run `pip --version` to check)
- A virtual environment (recommended)

### 1. Create a Virtual Environment

It is recommended to install viewephys in a virtual environment to avoid conflicts with other Python packages. 
> **Note:** viewephys is also compatible with the IBL Python environment.

Choose one of the following methods:

### Using Python venv

Create the environment:

```bash
python -m venv venv
```

Activate it on macOS or Linux:

```bash
source venv/bin/activate
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

### Using Conda

Create and activate a Conda environment:

```bash
conda create -n viewephys python=3.12
conda activate viewephys
```

### 2. Install viewephys

Choose one of the following methods:

### Install from PyPI

The latest release of viewephys is available on the Python Package Index (PyPI) with: 

```bash
pip install viewephys
```

### Install from Source

You can also install viewephys directly from a clone of the [Git repository](https://github.com/int-brain-lab/viewephys). This can be done either by cloning the repo and installing from the local clone, on simply installing directly via git.

```bash
git clone https://github.com/int-brain-lab/viewephys.git
cd viewephys
pip install .
```

### Editable Installation (Developers)

If you plan to modify the source code, install in editable mode:

```bash

pip install -e .

```

### 3. Verify the Installation

Confirm that viewephys is available from the command line:

```bash
viewephys --help
```

You should see output similar to:

```text

usage: viewephys [-h] [-f FILE]

Electrophysiology file viewer with preprocessing options

```

## Next Steps

Once installation is complete, continue with the

[Quickstart](quickstart) guide to learn how to launch viewephys and open your first recording.