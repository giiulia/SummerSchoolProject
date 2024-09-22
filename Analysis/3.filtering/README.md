Each algorithm has been tested both with a simple input and a single waveform to make sure any mistakes were carried into the implemetation. Studying how the same algorithms operate on multiple waveforms required multiple attempts since the computational steps are more and interchangeable.

# First filtering algorithm
The noise waveform is the difference between the original waveform (either the average or the reconstructed one 
from the average of the spectra, depending on in which domain the average has been done to get the filtered waveform) and the filtered waveform (the output of the filtering attempt)
> **Testing :** Noise waveform is compared to the expected waveform (a cosine wave with amplitude equal to the noise waveform's amplitude, frequency of the targeted component, 
phase depending on how the phase information is carried through that specific attempt).\

Some attempts refer to an expected noise waveform with an incorrectly-retrieved phase (see the [README from previous step](../2.two_combining_methods/README.md)), 
therefore even though the noise waveform obtained seems satisfactory, it is probably being compared to a non-existent component.

- Attempt one. Averaging the magnitudes $\longrightarrow$ filtering the average magnitude $\longrightarrow$ IFFT
  The expected noise waveform has a phase equal to the average of the phases of that component before filtering.
- Attempt two. Filtering 64 magnitudes $\longrightarrow$ averaging the filtered magnitudes $\longrightarrow$ IFFT
  The expected noise waveform has a phase equal to the average of the phases of that component before filtering.
- Attempt three. Filtering 64 magnitudes $\longrightarrow$ 64 IFFTs $\longrightarrow$ average the filtered waveforms
  The expected noise waveform has a phase equal to the average of the phases of that component before filtering.
- Attempt four. Filtering 64 spectra (complex) $\longrightarrow$ averaging the filtered spectra (complex) $\longrightarrow$ IFFT
  The expected noise waveform has a phase equal to the phase of the average of that component's measurements before filtering.


# Second filtering algorithm
The noise waveform can be retrieved is different ways. Each attempt r
- Attempt one. Averaging the magnitudes $\longrightarrow$ zeroing the average magnitude $\longrightarrow$ IFFT
- Attempt two. Zeroing 64 magnitudes $\longrightarrow$ averaging the zeroed magnitudes $\longrightarrow$ IFFT
- Attempt three. Zeroing 64 magnitudes $\longrightarrow$ IFFTs $\longrightarrow$ average the noise waveforms
- Attempt four. 
