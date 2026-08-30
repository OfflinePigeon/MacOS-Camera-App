# Camera App

A sleek, black-themed camera app for macOS — built with Python (OpenCV + Flask) and a native window via pywebview. Live viewfinder, digital zoom, grid overlay, and a film strip of your shots, all wrapped in a UI that looks like it belongs on your Mac.

> **macOS only.** This relies on AVFoundation for the camera feed and Finder/AppleScript for deleting photos, so it won't run as-is on Windows or Linux.

## Features

- Live camera feed in a native window (not a browser tab)
- Digital zoom slider (1x – 3x), with live preview while dragging
- One-click capture with shutter animation, saved as high-quality JPEGs
- Automatic sharpening pass on captured photos
- Rule-of-thirds grid overlay toggle
- Film strip of recent shots — click any thumbnail for a full-size preview
- Saves to folder named CameraApp (Not to be confused with the executable file camera_app)
- Delete photos straight from the app (moves to Trash, fully recoverable)
- One Finder shortcut to jump to your saved photos

## Setup

Clone or download this repo, then run once:

```bash
bash install.sh
```

This installs the Python dependencies and registers a global `camera` command.

## Usage

From any Terminal window:

```bash
camera
```

| Action | How |
|---|---|
| Take photo | Click the shutter, or press **Space** / **CMD+S** |
| Zoom | Drag the slider on the left, or use **Up / Down arrows** |
| Toggle grid | Click the grid icon, or press **CMD+G** |
| Preview a photo | Click its thumbnail in the film strip |
| Delete a photo | Open it, click **Delete**, confirm — moves to Trash |
| Open photos folder | Click the folder icon (top right of the viewfinder) |

## Where photos are saved

`~/Pictures/CameraApp/`, named `photo_YYYYMMDD_HHMMSS.jpg`.

## Requirements

- macOS with a built-in or connected webcam
- Python 3.9+
- Dependencies in `requirements.txt` (installed automatically by `install.sh`)

## First-time camera permission

The first time you launch the app, macOS may ask for camera access. If the feed stays black, check **System Settings -> Privacy & Security -> Camera** and make sure Terminal (or whichever app launches `camera`) is allowed.

