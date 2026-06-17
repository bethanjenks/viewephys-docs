# viewephys Documentation

This repository contains documentation for the viewephys electrophysiology viewer.

## Hosted Documentation

https://bethanjenks.github.io/viewephys-docs/

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
python -m webbrowser -t build/html/index.html
```