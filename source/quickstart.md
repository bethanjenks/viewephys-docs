# Quickstart Guide 
## Getting started 

viewephys can be used in two common workflows:

1. Open an existing recording to inspect previously acquired data.
2. Monitor a live recording during data acquisition.

This guide focuses on opening and navigating recordings in the graphical viewer.

## Open an Existing Recording

Use viewephys to explore previously acquired electrophysiology recordings.

Recordings can be loaded either:

- From the graphical interface
- Directly from the command line

### Open from the Graphical Interface

If you installed viewephys in a virtual environment as recommended, activate that environment before launching the viewer.

Start the viewer:

```bash
viewephys
```
The Ephys Bin Viewer window will open.

To load a recording:

1. Select **File → Open**.
2. Navigate to the desired binary recording (`.bin` file).
3. Open the file.


### Open from the Command Line
You can also load a specific recording directly when launching viewephys:

```bash
viewephys -f path/to/recording.ap.bin
```

For example:
```bash
viewephys -f examples/example_bin/1119617_LSE1_shank12_g0_t0.imec0.ap.bin
```

The recording will be loaded automatically when the viewer starts.

## Monitor a Live Recording

viewephys can also be used during data acquisition to monitor signal quality in real time.

1. Launch the viewer:

```bash
viewephys
```

2. Select **File → Open Live Recording**.

3. Navigate to the desired recording and select the corresponding `.bin` file.

Common uses include:

- Monitoring signal quality during acquisition
- Identifying noisy channels
- Verifying probe connectivity
- Checking recording stability