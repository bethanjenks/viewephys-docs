# Python API

viewephys can be launched directly from Python, allowing recordings and processed data to be visualized programmatically.

This is useful when working with:

- NumPy arrays
- Filtered recordings
- SpikeInterface outputs
- Custom analysis pipelines

When launching viewephys from a script, you need to create the Qt application yourself.

## Open a Binary File from Python

Use `EphysBinViewer` to open a binary recording file from a script.

```python

from viewephys.gui import EphysBinViewer, create_app

app = create_app()

viewer = EphysBinViewer("path/to/recording.ap.bin")

app.exec()

```

## View a NumPy Array

Use `viewephys()` to display data that is already loaded in Python.

```python

import numpy as np
from viewephys.gui import viewephys, create_app

app = create_app()

nc, ns, fs = (384, 50000, 30000)
data = np.random.randn(nc, ns) / 1e6

viewer = viewephys(data, fs=fs)

app.exec()

```

### Open Multiple Viewer Windows

Multiple viewer windows can be opened from the same Python session, allowing different datasets or processing stages to be compared side by side.

```python

import numpy as np
from viewephys.gui import viewephys, create_app

app = create_app()

nc, ns, fs = (384, 50000, 30000)
data = np.random.randn(nc, ns) / 1e6

viewer1 = viewephys(data, fs=fs)
viewer2 = viewephys(data * 50, fs=fs, title="Plot 2")

app.exec()

```