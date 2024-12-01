# Disclaimer
This Webapp works on and is optimized for **[Android]**!

This uses slightly different algorithms than SoundHoundPython, because the resources and library files are different.

The math behind the wave that generates the image is the same..

Output from this webapp can be verified with the built-in decoder.

I use github pages to test changes, the best time to clone this repo is at night US CST.

https://thehoundsoflove.github.io/SoundHoundWeb/

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

**Rendering information**

The brain calculates depth using difference fields primarily, but it has a fallback mode of calculating depth based on object size.

By interacting with objects and receiving sensory feedback, users can build a mental "library" of object sizes, shapes, and this will help it build depth cues. 

Over time, this library allows the brain to perform relative size and depth calculations more intuitively.

Additionally, as users repeatedly interact with specific objects, their brain creates associations between the tool's audio output and the actual size, shape, or position of those objects.

The brain uses this library to predict object properties without needing constant confirmation.

Once enough objects are in the library, users can extrapolate novel shapes or sizes by comparing them to familiar entries.

**Algorithms**

This tool does not have many algorithms used in sensory substitution because I intend for the brain to generate them with use.

For example, just starting at 50x50 resolution produces a faster wave, the benefit of this is to build algorithms for the association of objects.

In standard vision:

At 1 meter, two positions separated by 2 mm may be perceived as a single object moving smoothly if they change positions in less than around 20 ms

At 10 meters, this would correspond to roughly 2 cm.

100 meters, 20 cm.

This is why I have a 50x50 resolution option, the speed will make it so there is a fluid link between the data in frames that will cause the brain to recognize the disparate pieces of data as belonging to the same object.

By aligning spatial changes between frames with the thresholds of human motion perception, this ensures the brain interprets the input as belonging to the same object.
