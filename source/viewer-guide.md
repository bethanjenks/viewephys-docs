# Graphical User Interface

This page provides an overview of the viewephys graphical user interface (GUI) and its main features. You will learn how to navigate recordings, adjust display settings, inspect signals, and access additional visualization and analysis tools.

## Launching viewephys

viewephys can be launched from the command line, and recordings can be loaded either after the viewer starts or directly during launch.
To start the viewer without opening a recording:

```bash
viewephys
```

A recording can then be loaded through the graphical interface in the Menu bar (See in[Quickstart](quickstart)).
To open a recording immediately when launching viewephys, provide the file path using the `-f` option:

```bash
viewephys -f path/to/recording.ap.bin
```
The recording will be loaded automatically when the viewer starts.

> **Note:** viewephys can also be launched directly from a Python session. See the [Python API](python-api) page for details.

```bash
viewephys -f path/to/recording.ap.bin
```
For example:

```bash
viewephys -f examples/example_bin/1119617_LSE1_shank12_g0_t0.imec0.ap.bin
```

### Selecting a Data View

As described in the [Quickstart](quickstart) guide, viewephys provides several filtered representations of the same recording, including Raw, AP band, LF band, and AP band Destriped views.

The active data view can be selected from the **Ephys bin Viewier** menu.
The recording will be loaded automatically when the viewer starts.


## Interface Overview

The main viewer window provides tools for navigating electrophysiology recordings and inspecting signal quality.

![viewephys recording](images/viewephys_recording.png)

The interface is divided into several key areas:

1. **Menu Bar** – Access file operations, display options, and spike-picking tools.
2. **Display Controls** – Select channel metadata and switch between Density and Wiggle display modes.
3. **Gain Controls** – Adjust the signal gain to improve visibility of recorded activity.
4. **Signal Display** – The main viewing area, showing electrophysiology data across channels and time.
5. **Navigation Controls** – Scroll through time and channel ranges within the recording.
6. **Status Information** – Displays information about the current cursor position, including channel number, time, amplitude, and channel metadata.

The central panel displays electrophysiology data across channels and time.

- The x-axis is time.
- The y-axis is channels.
- Data are shown as a density map or traces.

## Navigating the Viewer

The viewer provides several tools for exploring recordings across time and channels.

### Navigation Controls

Use the horizontal and vertical scroll bars to move through the recording:

- The horizontal scroll bar moves forward and backward in time.
- The vertical scroll bar moves between channel ranges.

### Adjusting Signal Gain

The gain control can be used to increase or decrease signal visibility.

Gain can be adjusted using:

- The gain control in the viewer
- Ctrl + A or Page Up to increase gain by 3 dB
- Ctrl + Z or Page Down to decrease gain by 3 dB

### Keyboard Navigation

The arrow keys can be used to navigate recordings:

- ← and → move backward and forward through time
- ↑ and ↓ move between channel ranges
- Hold Ctrl while using the arrow keys to move in larger steps

### Cursor Information

Moving the cursor over the signal display updates the information panel with:

- Channel number
- Time
- Signal amplitude
- Channel metadata (if available)

## Display modes

viewephys provides several options for adjusting how recordings are displayed.

### Density Mode

Density mode displays signal amplitude as a 2D intensity map across channels and time.

### Wiggle Mode

Wiggle mode displays individual channels as trace plots, allowing detailed inspection of signal waveforms.

### Colour Maps

The appearance of the signal display can be customised using different colour maps.

To change the colour map:

1. Open the View menu.
2. Select Colourmap.
3. Choose a colour map from the available options.

Changing the colour map can improve visibility and make specific signal features easier to identify.

## Advanced Features

viewephys includes several additional tools for detailed inspection and analysis of recordings.

### Spike Picking Mode

Spike picking mode can be enabled from the **Pick** menu.
When spike picking mode is active:

- Left click – Add a spike marker
- `Shift` + Left click – Remove a spike marker
- `Ctrl` + Left click – Add a spike marker without wrapping around the maximum
- `Space` – Increment the spike group number

### Context Menu Tools

Additional inspection tools are available from the context menu within the signal display. These tools can be accessed by right-clicking within the recording display.

Available options include:

- **View Trace**
- **View Spectrum**
- **View Spectrogram**
