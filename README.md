# BFO Metal Detector and Differentiator

A fully analog metal detection system capable of detecting the presence of metals and distinguishing between ferromagnetic and diamagnetic materials using frequency shift analysis and signal processing.

## Overview

This project implements a **Beat Frequency Oscillator (BFO)-based metal detector** that not only detects metallic objects but also classifies them based on their magnetic properties.
Unlike conventional detectors, this system analyzes **frequency variations in oscillators** and converts them into **audible signals**, enabling intuitive real-time detection — all without using any microcontrollers.

![WhatsApp Image 2025-11-13 at 5 09 15 PM](https://github.com/user-attachments/assets/eefbc929-336b-4fda-b5ae-2553c750781b)
![breadboard_2](https://github.com/user-attachments/assets/a9a1d3bc-fd3b-4d99-b166-84764410efda)


## Features

- Detects presence of metallic objects  
- Differentiates between:
  - Ferromagnetic metals (iron, nickel, etc.)
  - Diamagnetic metals (copper, aluminum, etc.)  
- Fully analog design (no microcontroller required)  
- Real-time audible feedback using a speaker  
- Dual-mode operation:
  - Detection Mode
  - Differentiation Mode

## Working Principle

The system is based on two main oscillators:

### 1. ZVS(Zero Voltage Switching) Oscillator
- Generates a high-frequency sinusoidal signal (~25 kHz)
- Uses an LC tank circuit which consists of the search coil and capacitors
- Frequency changes when metal is brought near the coil

### 2. Schmitt Trigger Oscillator
- Generates a stable square wave
- Acts as a reference signal

### Signal Processing
- Signals from both oscillators are **multiplied**
- Produces **sum and difference frequencies**
- A **low-pass filter** extracts the difference frequency
- Comparators convert signals into sharp pulses
- Final output drives a **speaker for audible detection**

## Metal Differentiation Logic

| Material Type     | Effect on Inductance | Frequency Change | Output Sound |
|------------------|--------------------|------------------|--------------|
| Ferromagnetic    | Increases (L ↑)     | Frequency ↓       | Higher pitch |
| Diamagnetic      | Decreases (L ↓)     | Frequency ↑       | Lower/No sound |

## Circuit Diagram
<img width="1526" height="747" alt="circuit_diagram" src="https://github.com/user-attachments/assets/a11871d2-2f96-4be6-b108-8f774c1c97c3" />

## Components Used

- Resistors (various values)
- Capacitors (nF and µF range)
- Inductors (including search coil)
- IRFZ44 MOSFETs
- 2N3904 NPN Transistors
- LM358 Op-Amp
- LM393 Comparator
- Schottky Diodes (IN5822)
- Speaker

> 📄 Detailed component values and circuit diagrams are available in the project report.

## Applications

- Security screening systems  
- Industrial metal sorting  
- Underground cable/pipe detection  
- Archaeological exploration  
- Educational demonstrations

## Demo
📽️ Watch the demo: [https://youtu.be/YOUR_VIDEO_LINK](https://youtu.be/YWbpCmnJPQA)

## Team Members

- Rashid Rahman  
- Richu Mathew Shaji  
- Rishal Mohammed  

##  Documentation

Detailed explanation, circuit diagrams, and analysis are available in the project report.

## Future Improvements

- Improve sensitivity and detection range  
- Add digital display for frequency shift  
- Integrate microcontroller for visualization  
- Compact PCB-based design

## License

This project is for educational purposes.

⭐ If you found this project interesting, consider giving it a star!
