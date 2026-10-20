<h1 align="center">TCS3200 Colour Sensing</h1>
<p align="center"><strong>EMBEDDED SYSTEMS | OPTICAL SENSING</strong></p>
<p align="center"><a href="https://github.com/Kaveesha229">Kaveesha Gunawardena | Engineering portfolio</a></p>

## Overview

A compact colour sensing experiment using a TCS3200 sensor and Arduino Nano. It compares pulse durations for the red, green and blue filter selections and reports the channel with the shortest duration.

## Repository guide

<table>
<tr><th>File or folder</th><th>Purpose</th></tr>
<tr><td><a href="color.ino">color.ino</a></td><td>Main colour sensing sketch</td></tr>
</table>

## Hardware connections

<table>
<tr><th>TCS3200 signal</th><th>Arduino pin</th></tr>
<tr><td>S0</td><td>4</td></tr>
<tr><td>S1</td><td>5</td></tr>
<tr><td>S2</td><td>6</td></tr>
<tr><td>S3</td><td>7</td></tr>
<tr><td>OUT</td><td>8</td></tr>
</table>

## How it works

The sketch selects 20 percent output frequency scaling with S0 high and S1 low. It measures low pulse duration with `pulseIn` for each RGB filter and prints `R`, `G` or `B`. Equal minima produce no colour character. Characters are printed without a line break.

## Getting started

1. Open `color.ino` in Arduino IDE and select the connected Arduino Nano configuration.
2. Match the sensor wiring to the table.
3. Upload and open Serial Monitor at 9600 baud.
4. Present red, green and blue samples at a consistent distance under steady illumination.

## Implementation notes

The values are pulse durations rather than calibrated RGB intensities. The sketch has no white balance calibration, confidence threshold or explicit invalid reading handling. An LED output is not implemented in this version.

## Suggested verification

Record repeated measurements for each colour and a neutral reference. Check how lighting and distance change the decision before using it in sorting or robot control.

## Project media

Photos and demonstration videos will be added here as the project presentation is updated.

<p align="center"><sub>Practical engineering through building, testing and refinement.</sub></p>
