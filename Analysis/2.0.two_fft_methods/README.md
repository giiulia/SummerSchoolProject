## Method A
Computing the average of 64 waveforms $\longrightarrow$ FFT and phases of the reconstructed spectrum.

![Plot average waveform](070824_15.46/avg_wf_A.png)
![Plot average fft](070824_15.46/avg_fft_A.png)
Source code: [avg_wf_vs_avg_fft](avg_wf_VS_avg_fft-NOerrors.ipynb)
![Plot average phases](070824_15.46/avg_phases_A.png)
Source code: [avg_wf_vs_avg_phase](avg_wf_VS_avg_phase-NOerrors.ipynb) \
With this method you can see a chaotic phase composition in the averaged signal.

## Method B
Computing separetly the FFT of each waveform $\longrightarrow$ average FFT and average phases.\
Note that the average FFT is calculated by averaging the absolute values, but the phases must calculated before executing np.abs(Y), otherwise we would lose the phase information.

![Plot average fft](070824_15.46/avg_fft_B.png)
Source code: [avg_wf_vs_avg_fft](avg_wf_VS_avg_fft-NOerrors.ipynb)
![Plot average phases](070824_15.46/avg_phases_B.png)
Source code: [avg_wf_vs_avg_phase](avg_wf_VS_avg_phase-NOerrors.ipynb) \
With this method you can see a tendency towards an average phase of 0 degrees.

> **Naming convetions:** If the average is computed in time domain the average of the waveforms will be referred to as the average waveform, if the average is computed in frequency domain the average of the spectra will be referred to as the average FFT.
The term reconstructed refers to a waveform (or a spectrum) that is the inverse Fourier transform (or the Fourier transform) of an average in frequency (or time) domain.

## Comparison A VS B

![Plot A vs B](070824_15.46/A_VS_B.png)
Source code: [avg_wf_vs_avg_fft](avg_wf_VS_avg_fft-NOerrors.ipynb)
![Plot A vs B phases](070824_15.46/A_VS_B_phases.png)
Source code: [avg_wf_vs_avg_phase](avg_wf_VS_avg_phase-NOerrors.ipynb)
