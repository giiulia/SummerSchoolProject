- First step: characterize the radio background of my office at DESY to gain necessary expertise to apply the same analysis at RNO-G data.
   The main goal is to identify the sources with dominant magnitude in the high-frequency domain.
- Second step: filter any identified source using the information on its signal type: frequency and phase.

# 1. Spectral analysis
The background waveform is a superimposition of multiple sine waves, each of them described by a frequency and a phase.\
* The Fourier Transform of a waveform discloses the frequency components of the signal.
* The output of the Fourier transform is a set complex numbers, the angles associated to those numbers in the complex plane are the phases of the signal's components.

How to compute the Fourier transform of a waveform: discrete Fourier transforms are implemented in the Python [FFT package](https://docs.scipy.org/doc/scipy/reference/fft.html#).\

 ![Plot waveform](070824_15.46/wf.png)  ![Plot dft](070824_15.46/dft.png) 

The data acquisition system provided the possibility to save a maximum of 64 waveforms. There are in principle two ways one can extract the DFT from this input.


