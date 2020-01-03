# AudioForma Fingerprint Experimental Design

Information Design: Ning Chen
Technical Support: Tianyu Liu

## Introduction
AudioForma is an audio analysis web app designed and developed by Ning Chen, Jasper Croome, and Rebecca Lantner. The goal is to creatively add a visual dimension to a given aural experience.
- The first part of the app lets users revisit their Spotify music library with a refreshing experience. It visualizes the grouping of songs according to their metadata such as title, artist, and genre. "Sort function" is used to rearrange songs by popularity, danceability, etc which are Spotify-unique data attributes. Make sure you have registered on Spotify, added several favorite songs to your library. Go to `https://audioforma.herokuapp.com/` to authorize AudioForma to access your Spotify library.
- This repository constitutes the second part of the app, a song fingerprint experimental design.

## Quick start

#### Preparation
+ Make sure you have installed Python 3.6+ on your local PC.
+ Double-click the `run_webserver.bat` script to run the server. Visit `http://localhost:8000/`.

#### Run the app
+ Click the `start` button. Once it changes from `loading` to `loaded`, the 30 second music and the dynamic visualization simultaneously begin.
+ The real-time rendering captures up to 12 possible notes across 8 possible octaves. The 30 seconds of audio "traces" consist of a stack of Gaussian curves each representing a note’s intensity at a given time.

## Instructions on how to produce your own music fingerprint
AudioForma's raw data is produced by `librosa` audio analysis library.
For the best visualization result, it is highly recommended that the length of music be kept under 30 seconds.

To install `librosa` on Windows:
- Run `pip install librosa`
- Install `ffmpeg` binary
  + Download `ffmpeg` binary from `https://www.ffmpeg.org/download.html#build-windows`
  + Extract the files to a certain folder, e.g. `C:\Program Files\FFMPEG`
  + Set user environment variable such that `PATH` includes `C:\Program Files\FFMPEG`
  + Sign off and re-log in Windows to make environment variable take effect
- Run `AnalyzeMusic.py` to analayze audio file and store the output as CSV file in the same folder.
- Update the file names in line 13 and 15 in the `main.js`.

## Special thanks
Our special thanks go to Zona Kostic for her creative and strategic direction.

## Sample music copyright
Celtic Suite by Roberto Di Marino.
