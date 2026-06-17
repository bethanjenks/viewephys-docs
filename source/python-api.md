# Python API

viewephys can be launched directly from a Python session to visualize binary recordings, NumPy arrays, and data generated during analysis workflows.

This page covers two common ways to use viewephys from Python:

* launching viewephys from an interactive Python session, such as IPython or Jupyter
* launching viewephys from a standalone Python script

## Interactive Python Session

In an interactive Python session, viewephys can be used to display data that is already loaded in memory as a NumPy array.

If you are using IPython or Jupyter, you may first need to enable the Qt event loop:

```python
%gui qt
```
Then load and display your data:

```python
import numpy as np
from viewephys.gui import viewephys

nc, ns, fs = (384, 50000, 30000)  # channels, samples, sampling rate in Hz
data = np.random.randn(nc, ns) / 1e6  # example data in volts

ve = viewephys(data, fs=fs)
```

viewephys expects array data in the shape:

```python
(n_channels, n_samples)
```
The sampling rate must be provided using fs, in Hz.

### Opening Multiple Windows 

Multiple viewer windows can be opened from the same Python session. Each window must be given a different title:

```python
ve1 = viewephys(data, fs=fs, title="raw data")
ve2 = viewephys(data * 50, fs=fs, title="scaled data")
```
If the same title is reused, viewephys updates the existing window instead of opening a new one.

## Launching from a Python Script

When using viewephys from a standalone Python script, you need to create the Qt application before opening the viewer and start the Qt event loop at the end of the script.

## Open a Binary File 

Use `EphysBinViewer` to open a binary recording file from a script.

```python

from pathlib import Path
from viewephys.gui import EphysBinViewer, create_app

app = create_app()

viewer = EphysBinViewer(Path("path/to/recording.ap.bin"))

app.exec()

```

## Display a NumPy Array

Use `viewephys()` to display data that is already loaded in Python.

```python
import numpy as np
from viewephys.gui import viewephys, create_app

app = create_app()

nc, ns, fs = (384, 50000, 30000) # channels, samples, sampling rate in Hz
data = np.random.randn(nc, ns) / 1e6 # example data in volts

ve = viewephys(data, fs=fs)

app.exec()
```

### Array shape
viewephys expects NumPy arrays to be arranged as:

```python
(n_channels, n_samples)
```
Some tools return data in a different order. For example, SpikeInterface typically returns traces as:
```python
(n_samples, n_channels)
```
In this case, transpose the array before passing it to viewephys:

```python
data = data.T
ve = viewephys(data, fs=fs)
```
### Optional Parameters

The viewephys() function requires:

* data: a NumPy array with shape (n_channels, n_samples)
* fs: the sampling rate in Hz

Optional parameters include:

* channels: channel information, such as probe geometry
* title: title of the viewer window
* t0: start-time offset
* colormap: colormap used for display

If no channel information is provided, viewephys uses a default Neuropixels version 1 layout. For non-NP1 probes or custom recordings, you may need to provide channel information manually.