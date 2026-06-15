# Documentation Review Notes

## Installation

### Issue 1: Python version

Draft documentation:
- Python 3.8 or higher

Observed:
- Installation failed on Python 3.9.19
- Package requires Python >= 3.10

Recommendation:
- Update installation requirements.

---

## CLI

### Issue 2: Launch command

Draft documentation:
```bash
viewephys path/to/data.bin
```

Observed:
```bash
viewephys -f path/to/data.bin
```

Recommendation:
- Verify current CLI syntax and update examples.
```

---
## Loading data in python

### Issue 3: ### Python usage example is incorrect

Draft documentation suggests:

```python
from viewephys import viewephys
viewephys("path/to/file.bin")

TypeError: 'module' object is not callable

Fix:

from pathlib import Path
from viewephys.gui import EphysBinViewer, create_app
app = create_app()
viewer = EphysBinViewer(
    Path("recording.ap.bin")
)

app.exec()

* create_app() creates the GUI application
* EphysBinViewer loads the binary file
* app.exec() starts the event loop

This is an alternative to starting the viewer through the command line.
--- 

## View Data Already Loaded in Python

If your data has already been loaded or preprocessed in Python, you can display it directly in viewephys without opening a binary file.

For example, the code below loads electrophysiology data using SpikeInterface, applies preprocessing, and displays the result in viewephys.

```python
from viewephys.gui import create_app, viewephys

app = create_app()

# data must have shape (channels, timepoints)
data = my_data

viewer = viewephys(
    data,
    fs=30000,
    title="Example recording"
)

app.exec()
```

### Array Format

When displaying data from Python, viewephys expects arrays with shape:

```text
(channels, timepoints)
```

Some libraries return data as:

```text
(timepoints, channels)
```

In this case, transpose the array before passing it to viewephys:

```python
data = data.T
```

## GUI Documentation

### Missing

- Explanation of signal types
- Explanation of Dataset Info panel
- Time navigation
- Typical workflows

Recommendation:
- Add GUI guide with screenshots.

---

## Workflows

### Missing

- Live recording monitoring
- Reviewing completed recordings

Recommendation:
- Add task-based examples.

---

## Future Improvements

- PSTH example (mentioned in recent issue)
- More screenshots
- FAQ
- Troubleshooting section