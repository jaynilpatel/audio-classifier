# GTZAN-music-speech-classifier
A deep audio classifier that is capable of classifying an audio as music or speech. The dataset consists of 128 tracks, each 30 seconds long. Each class (music/speech) has 64 examples. The tracks are all 22050Hz Mono 16-bit audio files in .wav format. 

The raw audio is processed using discrete Fourier transform. This will return complex coordinates (real and imaginary) which will be then converted into cartesian coordinates indicating magnitude and phase. 

The final pre-processing step will be to plot a logarithmic perception of sound. A sliding window is created that will snap the Xs and ys of the graph and will store in a list as inputs to the network. All the collected inputs and labels will then be fed to a 4 layer CNN + 2 fully connected layer model.

 
