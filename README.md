# viewephys Documentation

This repository contains documentation for the viewephys electrophysiology viewer.

## Build Locally

Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate
```

Install documentation dependencies:

```bash
pip install -r requirements.txt
```

Build the documentation:

```bash
make html
```

Open the generated site:

```bash
open build/html/index.html
```