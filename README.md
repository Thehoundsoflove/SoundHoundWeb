# Disclaimer
This Webapp works on and is optimized for **[Android]**!

Output from this webapp can be verified with the built-in decoder.

I will no longer use github pages to test changes, as this app has begun the live testing phase of development.

https://thehoundsoflove.github.io/SoundHoundWeb/

# SoundHound Webapp

SoundHound is a **prototype**, it is a Sensory Substitution tool that has a default resolution of 350x350 but is can be downscaled to as low as 50x50.

This tool is very different from available sensory substitution options in the following ways:

- Depth information is completely virtualized and relayed in mono.
- Aimed toward mono users.
- Uses a square wave, but has other wave options.

I have made this opensource so others can use this code as they see fit.

That being said, there are a lot of unknowns in regard to using a square wave to render a soundscape. I think this prototype might be the first of its kind.

**Image Capturing**

Edge Detection: Uses the Sobel edge detection algorithm to detect edges in the captured image, which is then used to create grayscale values.

Grayscale Conversion: The edges from the Sobel operator are converted into grayscale values, with detected edges being represented in white (255) and non-edges as black (0).

Audio Generation: The grayscale values are then mapped to frequencies to generate sine wave audio. The amplitude of each sine wave is proportional to the pixel's brightness value.

**Audio output**

The audio generation converts the grayscale values of each pixel into different wave frequencies.

Each grayscale value corresponds to a frequency between 20 Hz and 20,000 Hz, which are used to modulate the audio signal.

The app generates a WAV audio file from the wave used and plays it using an <audio> element.

Audio normalization is applied to ensure the amplitude does not exceed the maximum range.

**Audio encoding**

The generated audio has a sample rate of 44,100 Hz.

Each pixel in the image corresponds to a single audio sample (1 sample = 1 pixel), and the duration of each sample is approximately 22ish microseconds.

**Depth**

The brain calculates depth using difference fields primarily, but it has a fallback mode of calculating depth based on object size.

By interacting with objects and receiving sensory feedback, users can build a mental "library" of object sizes, shapes, and this will help it build depth cues. 

Over time, this library allows the brain to perform relative size and depth calculations more intuitively.

To assist with the creation of this library, I have added an algorithm to create a virtual depth map.

As users repeatedly interact with specific objects, their brain creates associations between the tool's audio output and the actual size, shape, or position of those objects.

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

By aligning spatial changes between frames within the thresholds of human motion perception, this ensures the brain interprets the input as belonging to the same object.

**Examples**

Just convert an image to Grayscale, that's how accurate the representation is.
