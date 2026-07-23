# FPT Introduction
The demo system is architected as a **modular, scalable RF measurement platform** designed to operate across both **Lite** and **Pro** hardware versions while supporting **manual SFP‑based workflows** and **fully automated TestStand sequences**. The architecture integrates NI’s measurement software ecosystem—**RFmx**, **InstrumentStudio**, and **TestStand**—with application libraries developed by **ADG SRD**, including the **PAEML** and **SPML** libraries, to deliver a unified and reusable measurement framework.

## Measurement List
Small Signal CW and Pulsed S-Parameters
- Vector Calibration with ECal
- Select Stimulus Waveform (CW or Pulsed)
- Switch PA on and Measure S11 and S21 from 8-12 GHz.
- Switch LNA on and Measure S22 and S21 from 8-12 GHz.
- Graph S-Parameters Using 4-Quadrant or Individual Graphs.

Large Signal CW and Pulsed S-Parameters
- Vector Calibration with manual calkit (Maury)
- Select Stimulus Waveform (CW or Pulsed)
- Switch PA on and Measure S11 and S21 from 8-12 GHz.
- Switch LNA on and Measure S22 and S21 from 8-12 GHz.
- Graph S-Parameters Using 4-Quadrant or Individual Graphs.

Power Compression
- No Calibration – Compensate Using Pre-Measured Cable Loss
- Select Stimulus Waveform (CW or Pulsed)
- Switch PA on and Sweep Power at TX_IN for 8, 10, and 12 GHz.  Measure Power at ANT for Each Frequency.
- Switch LNA on and Sweep Power at ANT for 8, 10, and 12 GHz.  Measure Power at RX_OUT.
- Graph Input Power vs. Output Power, Gain, and P1dB, P3dB, etc. for all 3 Frequencies.

Intermodulation and TOI – VST & RFmx SpecAn
- No Calibration – Compensate Using Pre-Measured Cable Loss
- Select Sweep Type – Power, Frequency, or Tone Spacing
- Sweep Fundamental Signals and Measure Output Power of Fundamental and Intermods
- Graph Output Power of Fundamental and Intermods and Gain (Separate Graphs), and Extrapolate TOI

Noise Figure – VST, Synthetic Noise Source, and RFmx Noise Figure
- Calibrate Using Loopback from VST RF Out to RF In
- Following VST Setup Including BW, Interval, Frequencies, Max Gain, Max NF
- Switch LNA On and Measure NF at 7GHz to 12GHz with 200MHz step size.
- Graph NF over Frequency

Noise Figure – VST, External Noise Source (NC346x), and RFmx Noise Figure
- Calibrate by directly connecting NC346x to VNA port-1.
- Following VST Setup Including BW, Interval, Frequencies, Max Gain, Max NF
- Switch LNA On and Measure NF at 7GHz to 12GHz with 200MHz step size.
- Graph NF over Frequency

Pulse Measurements
- No Calibration – Compensate Using Pre-Measured Cable Loss
- Following VST Setup Including Center Frequency, Measurement BW, Reference Level, Pulse Power Level, Length, PRI.
- Drive Pulse RF and Measure Pulse Metrics and Pulse Stability
- Graph Intra-Pulse Stability, Pulse-to-Pulse Stability, and Acquired Amplitude.

## Hardware
- NI PXIe-1095 x1
- NI PXIe-5842 x1
- NI PXIe-5655 x1
- NI PXIe-5633 x1
- NI PXIe-2599 x3
- NI PXIe-2597 x1
- NI PXIe-4139 x2
- NI PXIe-4147 x1
- NI PXIe-4142 x1
- NI PXIe-6571 x1
- NI CAL-5501 x1
- External Noise Source (NC346C) X1
- 20dB attenuator (BW-S20W20+) x1
- 20dB coupler (C1-C31-20 RD Microwave Couplers) x4
- Mechanical SOLT calibration kit x1

**Depending on the DUT, you may not need all the NI PXI cards.**

add a photo of NI MAX

## Software
- LabVIEW 2023Q3
- niRFmx 26Q1
- niRFSA 26Q1
- niRFSG 26Q1
- niDCPower 26Q1
- niDigital 26Q1
- niSwitch 2023Q3
- ni SPML 2023
- ni PAEML 2023
- Measurement Plug-in SDK 3.5.4.1


## Creating your own
You will find a folder named "Framework". Use that as the starting point to create your project. 
