# FMCW Doppler Radar using PlutoSDR and Log-Periodic Antenna

## Project Overview
This project implements a **Doppler radar system** using the **Analog Devices PlutoSDR** and a **log-periodic antenna**.  
By transmitting **FMCW (Frequency Modulated Continuous Wave) chirp signals** and analyzing the received reflections, the system detects motion and extracts **Doppler frequency shifts** in real time.

## Features
- FMCW chirp signal generation using **GNU Radio**.
- Real-time transmit/receive using **PlutoSDR** hardware.  
- Doppler frequency shift extraction for **motion detection**.  
- Visualization with **time–frequency plots, spectrograms, and FFT analysis**.  
- Custom RF front-end with **log-periodic antenna** for wideband operation.  

## Hardware & Software
**Hardware:**
- [ADALM-PlutoSDR](https://wiki.analog.com/university/tools/pluto)
- Log-Periodic Antenna  
- Coaxial cables, RF connectors  

**Software:**
- [GNU Radio](https://www.gnuradio.org/)  
- PlutoSDR IIO drivers  
- Python (for additional data processing and plotting)  

## System Architecture
1. **Signal Generation:** FMCW chirp signals generated in GNU Radio.  
2. **Transmission:** PlutoSDR transmits chirps via log-periodic antenna.  
3. **Reception:** Reflected signals captured by PlutoSDR.  
4. **Processing:** Beat frequency extraction using low-pass and band-reject filtering.  
5. **Visualization:** Time-domain, frequency-domain, and spectrogram plots display Doppler shifts.  

## Benefits of FMCW
- Provides **high range resolution** due to large signal bandwidth.  
- Enables **simultaneous range and velocity measurement** (via beat frequency analysis).  
- Continuous transmission → **no dead zones** compared to pulsed radar.  
- Lower **power requirements** compared to pulsed radar systems.  
- Easier to implement in **low-cost SDR hardware** such as PlutoSDR.  
