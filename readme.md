# AudioForma Fingerprint Experimental Design

Information Design: Ning Chen
Technical Support: Tianyu Liu

## Introduction
AudioForma is an audio analysis web app designed and developed by Ning Chen, Jasper Croome, and Rebecca Lantner. The goal is to add a visual dimension to an audio experience.
- The first part of the app let users explore their Spotify music library and select a song to hear and view in detail. This visualization hinged on song “metadata” like title, artist, and genre. Before exploration, make sure you have registered Spotify, save several favorite songs to your library. Go to `https://audioforma.herokuapp.com/`to authorize AudioForma the rights to access your Spotify library.
- Files in this repository present the second part of the app, a song fingerprint experimental design. 

## Quick start

#### Preparation
+ Make sure you have Python 3.7+ installed on your local pc.
+ Double-click the `run_webserver.bat` script to run the server. Visit `http://localhost:8000/`.

#### Run the app
+ click on the `start` button, when it changes from `loading` to `loaded`, the 30 second music starts to play, and the visualization begins to build.
+ The real-time rendering captures up to 12 possible notes across 8 possible octaves. The visual result shows 30 seconds of audio "traces", each curve representing a note’s intensity at a given time and accumulating into a stacked, Gaussian fingerprint.

## Instructions on how to produce your own music fingerprint
AudioForma's data level results are produced by Librosa audio analysis library.
To get the best visualization result, it is highly recommended that the length of music should be under 30 seconds.

To install `librosa` on Windows:
- Run `pip install librosa`
- Install `ffmpeg` binary
  + Download `ffmpeg` binary from `https://www.ffmpeg.org/download.html#build-windows`
  + Extract the files to a certain folder, e.g. `C:\Program Files\FFMPEG`
  + Set user environment variable such that `PATH` includes `C:\Program Files\FFMPEG`
  + Sign off and re-log in
- Run `AnalyzeMusic.py` to manually convert audio file, and store the output in CSV form in the same folder.
- Update the file names in line 13 and 15 in the `main.js`.

## Special thanks
Our special thanks goes to Zona Kostic for her creative and strategic direction.

## Sample music copyright
Celtic Suite by Roberto Di Marino.
