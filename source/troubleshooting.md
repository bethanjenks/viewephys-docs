# Troubleshooting

**Viewer Does Not Launch**

If `viewephys` does not start:

- Verify that the package is installed correctly.
- Ensure you are working in the correct Python environment.
- Check that all dependencies were installed successfully.

Try confirming the installation:

```bash
viewephys --help
```

**Command Not Found**

If your terminal reports:

```text
viewephys: command not found
```

make sure:

- The environment containing viewephys is activated.
- The installation completed successfully.

You can verify the installation with:

```bash
pip show viewephys
```

**File Not Found**

If a recording cannot be opened:

- Verify that the file path is correct.
- Check that the recording file exists.
- Ensure you have permission to access the file.

**Python Viewer Does Not Appear**

When launching viewephys from a Python script, make sure a Qt application is created before opening the viewer:

```python
from viewephys.gui import create_app

app = create_app()
```

and that the event loop is started:

```python
app.exec()
```

**Unexpected Data Orientation**

When displaying NumPy arrays, data should be arranged as:

```text
channels x timepoints
```
If your data is arranged as:

```text
timepoints x channels
```
transpose the array before displaying it:

```python
data = data.T
```

*** Need More Help?***

If you encounter an issue that is not covered here, check the viewephys [Git repository](https://github.com/int-brain-lab/viewephys) for updates and open issues. 