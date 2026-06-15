# Installation

## Requirements

Before installing viewephys, ensure you have:

- Python 3.10 or later
- A virtual environment (recommended)

> **Note:** Installing with Python versions earlier than 3.10 may result in installation errors.

## 1. Create a Virtual Environment (Recommended)

It is recommended to install viewephys in a virtual environment to avoid conflicts with other Python packages.

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
> **Note:** viewephys is also compatible with the standard IBL Python environment.

## 2. Install viewephys

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

The `-e` flag allows changes to the source code to be reflected immediately without reinstalling the package.

## 3. Verify the Installation

Confirm that viewephys is available from the command line:

```bash
viewephys --help
```

You should see output similar to:

```text

usage: viewephys [-h] [-f FILE]

Electrophysiology file viewer with preprocessing options

```

