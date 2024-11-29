# Disclaimer
This Webapp works on and is optimized for **[Android]**!

This uses slightly different algorithms than SoundHoundPython, because the resources and library files are different.

The math behind the wave that generates the image is the same..

Output from this webapp can be verified with the built-in decoder.

# SoundHound Webapp
SoundHound is a pet project, it is a Sensory Substitution tool that has a very high resolution of 350x350.

**Image Capturing**
Edge Detection: Uses the Sobel edge detection algorithm to detect edges in the captured image, which is then used to create grayscale values.

Grayscale Conversion: The edges from the Sobel operator are converted into grayscale values, with detected edges being represented in white (255) and non-edges as black (0).

Audio Generation: The grayscale values are then mapped to frequencies to generate sine wave audio. The amplitude of each sine wave is proportional to the pixel's brightness value.

**Audio output**
The audio generation converts the grayscale values of each pixel into sine wave frequencies.

Each grayscale value corresponds to a frequency between 20 Hz and 20,000 Hz, which are used to modulate the audio signal.

The app generates a WAV audio file from the sine wave and plays it using an <audio> element.

Audio normalization is applied to ensure the amplitude does not exceed the maximum range.

**Audio encoding**
The generated audio has a sample rate of 44,100 Hz.

Each pixel in the image corresponds to a single audio sample (1 sample = 1 pixel), and the duration of each sample is approximately 22ish microseconds.

The sine wave frequencies range from 20 Hz to 20,000 Hz, mapped based on the grayscale values of the image pixels.

**Examples**

<img width="361" alt="image" src="https://github.com/user-attachments/assets/42c7991b-88c3-4063-bb3e-228f109336fa">

<img width="384" alt="Screenshot 2024-11-28 at 10 53 27 AM" src="https://github.com/user-attachments/assets/7ecf62e4-0f40-4455-a911-554c4db68f3a">
