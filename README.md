# Wireless MP4 Video Transmission using GNU Radio and USRP B210
## Video Link: https://drive.google.com/file/d/1CB-UP1ENmAED2txfIvJdk1YfVAcLLJMw/view?usp=sharing
## Overview

As part of our M.Tech lab project at IIT Bhubaneswar, our team implemented an end-to-end wireless video transmission system using:

- GNU Radio Companion (GRC)
- Software Defined Radio (SDR)
- USRP B210 hardware
- BPSK digital modulation

The system successfully transmitted and recovered an MP4 video wirelessly over the air at:

```text
905.2 MHz
```

using real RF hardware communication.

---

# Project Highlights

✅ End-to-end wireless MP4 transmission  
✅ Real-time SDR implementation  
✅ BPSK differential modulation  
✅ CRC32 packet verification  
✅ Symbol synchronization and carrier recovery  
✅ Successful wireless video recovery over RF channel  

---

# System Specifications

| Parameter | Value |
|---|---|
| Modulation | BPSK |
| Carrier Frequency | 905.2 MHz |
| SDR Hardware | USRP B210 |
| Communication Distance | 25 cm |
| Platform | GNU Radio Companion |
| Channel | Wireless RF |
| Packet Size | 64 Bytes |
| Error Detection | CRC32 |
| Pulse Shaping | Root Raised Cosine (RRC) |

---

# Hardware Used

- 2 × USRP B210 SDR boards
- Dipole antennas
- 2 laptops
- GNU Radio
- UHD drivers


---

# Complete System Flow

## End-to-End Communication Pipeline

<img width="1668" height="943" alt="flowchart" src="https://github.com/user-attachments/assets/0211162d-f107-4e2e-a0b5-bca4d3b66648" />


### Transmitter (TX)
The transmitter performs:
- MP4 file reading
- Packet formation
- CRC generation
- Protocol framing
- Differential BPSK modulation
- RF transmission using USRP B210

### Wireless Channel
The transmitted signal propagates through:
- free-space channel
- noise
- multipath effects

### Receiver (RX)
The receiver performs:
- matched filtering
- symbol synchronization
- carrier recovery
- packet synchronization
- CRC verification
- MP4 reconstruction

---

# Physical Experimental Setup

## SDR Hardware Setup

<img width="720" height="1280" alt="Physical set up" src="https://github.com/user-attachments/assets/6e1a8b6f-9117-435e-af8f-2e7b8d280968" />

The experimental setup consists of:
- two USRP B210 SDRs
- separate TX and RX systems
- dipole antennas
- over-the-air RF transmission

Transmission was successfully demonstrated inside the RF lab environment.

---

# GNU Radio Transmitter Flowgraph

## TX Design

<img width="1065" height="412" alt="Tx" src="https://github.com/user-attachments/assets/90a2d384-1192-4a5f-922c-523cd7a343cf" />


### Main Processing Blocks

- File Source
- Packet Framing
- CRC32 Generator
- Differential Encoder
- BPSK Modulator
- RRC Pulse Shaping
- UHD USRP Sink

---

# Transmitted Signal Waveform

## TX Signal

<img width="1600" height="897" alt="Tx waveform" src="https://github.com/user-attachments/assets/782036ba-797e-463c-9587-7b7ee263181c" />


### Observations
- Proper BPSK symbol generation observed
- Pulse-shaped waveform using RRC filter
- Stable transmission characteristics achieved

---

# GNU Radio Receiver Flowgraph

## RX Design

<img width="1600" height="900" alt="rx" src="https://github.com/user-attachments/assets/ffb9e394-f776-4a36-ab85-f04b12dfdfc7" />


### Main Receiver Blocks

- UHD USRP Source
- RRC Matched Filter
- Symbol Synchronization
- Costas Loop
- Differential Decoder
- Packet Detection
- CRC Verification
- File Reconstruction

---

# Received Signal Waveform

## RX Signal

<img width="1920" height="1080" alt="Rx waveform" src="https://github.com/user-attachments/assets/933875a5-f7f6-40ee-ad69-60eacc593d29" />


### Observations
- Successful symbol recovery achieved
- Proper synchronization observed
- Stable demodulated waveform obtained

---

# Key DSP Components

## 1. Differential BPSK Modulation

Used for robust phase ambiguity handling.

### BPSK Signal

:contentReference[oaicite:0]{index=0}

---

## 2. Root Raised Cosine (RRC) Filter

Used for:
- pulse shaping
- ISI reduction
- matched filtering

---

## 3. Symbol Synchronization

Implemented using:
- TED (Timing Error Detector)
- MMSE interpolation

---

## 4. Costas Loop

Used for:
- carrier phase recovery
- coherent demodulation

---

## 5. CRC32 Verification

Ensures:
- packet integrity
- corrupted packet rejection

---

# Experimental Results

✅ Successful wireless MP4 transmission achieved  
✅ Stable BPSK modulation and demodulation  
✅ Accurate symbol synchronization  
✅ Proper carrier recovery using Costas Loop  
✅ CRC-based packet verification successful  
✅ Video reconstructed successfully at receiver  

---

---



This project helped in understanding:

- Software Defined Radio (SDR)
- GNU Radio Companion
- Digital communication systems
- BPSK modulation
- Carrier recovery
- Symbol synchronization
- Packet framing
- Error detection using CRC
- RF transmission using USRP

---

# Applications

This type of SDR communication system can be extended for:

- Wireless multimedia transmission
- Cognitive radio
- Tactical communication
- Satellite communication
- IoT communication systems
- SDR-based research platforms

---

# Future Improvements

Possible future extensions:
- QPSK / QAM modulation
- FEC coding
- OFDM transmission
- Long-distance communication
- Real-time streaming
- Adaptive modulation

---

# Conclusion

A complete wireless video transmission system was successfully implemented using GNU Radio and USRP B210 SDR hardware.

The project demonstrated:
- reliable BPSK wireless communication
- synchronization techniques
- packetized MP4 transmission
- successful RF video recovery

This project provided hands-on experience in practical SDR-based wireless communication systems.

---

# Authors

Suman Das  
M.Tech Student  
IIT Bhubaneswar
