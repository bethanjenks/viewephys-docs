# Troubleshooting

If you encounter problems while installing or using viewephys, the following sections describe common issues and their solutions.

## Support

If your issue is not covered here, you can:

- Search existing issues on the viewephys GitHub repository.
- Open a new issue in the repositiory. 

GitHub repository:
[viewephys](https://github.com/int-brain-lab/viewephys)


## Common Issues 

### Viewer Does Not Launch 

If `viewephys` does not start:

- Verify that the package is installed correctly.
- Ensure you are working in the correct Python environment.
- Check that all dependencies were installed successfully.

Try confirming the installation:

```bash
viewephys --help
```

### File Not Found

If a recording cannot be opened:

- Verify that the file path is correct.
- Check that the recording file exists.
- Ensure you have permission to access the file.

### Incorrect visualization of Data

- Verify number of channels and sampling rate
- check the selected data view for filtering options 

### Python Viewer Does Not Appear

When launching viewephys from an a Python script, make sure a Qt application is created before opening the viewer:

```python
from viewephys.gui import create_app

app = create_app()
```

and that the event loop is started:

```python
app.exec()
```
