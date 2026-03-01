# music-visualizer

🎵 Circular Music Visualizer

A real-time 3D circular music visualizer built using Three.js and the Web Audio API.
This project analyzes audio frequency data and renders a dynamic radial spectrum that reacts smoothly to music with cinematic lighting and glow effects.

🚀 Short Description

A browser-based 3D circular spectrum visualizer that maps real-time FFT frequency bins to animated bars arranged in a ring. Features smooth interpolation, reactive lighting, and atmospheric rendering — all in a single HTML file.

✨ Features

64 frequency bars arranged in a circular layout

Real-time FFT analysis using Web Audio API

Smooth bar animation using linear interpolation (LERP)

Emissive glow based on audio intensity

Reactive center pulse light

Cinematic fog and multi-light setup

Fully browser-based (no build tools required)

Single-file implementation

🛠 Tech Stack

Three.js (r128) — 3D Rendering

Web Audio API — Audio Analysis

HTML / CSS / JavaScript

📂 Project Structure
music-visualizer/
 ├── index.html
 └── README.md

Everything runs from index.html.

▶️ How to Run

Download or clone the repository

Open index.html in your browser
OR
Use VS Code Live Server

Upload any audio file

Enjoy the visualization

No installation required.

🎛 How It Works

Audio file is decoded using AudioContext

AnalyserNode performs FFT (Fast Fourier Transform)

Frequency bin data is stored in a Uint8Array

Each bar corresponds to one frequency bin

Bar height scales according to amplitude

Smooth motion is achieved using linear interpolation:

current += (target - current) * LERP

Lighting intensity reacts to overall audio energy

⚙️ Customization

You can easily modify:

BAR_COUNT → number of spectrum bars

RADIUS → circle size

LERP → smoothing speed

fftSize → frequency resolution

Light colors and intensity

Camera position and tilt

🔮 Future Improvements

Beat detection with peak tracking

Bloom post-processing

GPU instanced bars for higher performance

Shader-based deformation

Microphone input support

Color cycling based on frequency bands

Camera orbit animation

Export visualization as video

🧠 Architecture Overview
Audio Input
   ↓
AudioContext
   ↓
AnalyserNode (FFT)
   ↓
Uint8Array Frequency Data
   ↓
Three.js Render Loop
   ↓
Circular Bar Scaling + Lighting Reaction
