# Disclaimer
This Webapp works on and is optimized for **[Android]** and **[iPhone iOS 18~]!**
 - iPhone note: Use Brave Browser, it will not work with any other browser.
 - iPhone note: Maximum of 250x250 resolution.

Output from this webapp can be verified with the built-in decoder.

I will no longer use github pages to test changes, just to update the tool as it is used and feedback is given on it.

For example, I never intended to have to make a square wave analog, but after testing it the square wave was just too unintuitive and the brain could not really make actionable sense of it. The learning curve was just too high.

Pulses based around the principle of a square wave mimic the natural firing of neurons, so information is presented to the brain in a highly familiar way and it really shows as there seems to be a natural compatibility between the input received and the usability of it, despite the extremely high speed it is relayed at.

This app has begun the live testing phase of development.

https://thehoundsoflove.github.io/SoundHoundWeb/

# SoundHound Webapp

**Pulse Mapping:**

The system converts visual information into 22 microsecond pulses per pixel, with the length and intensity of the pulses correlating to visual characteristics like brightness and depth.
The pulses convey detailed data, often undetectable by the conscious mind but still perceivable by the brain through auditory processing.

The brain is highly attuned to changes in time and temporal patterns. Short, discrete pulses can provide information in a form that the brain can quickly identify and process.

Under this, with zero training it is possible for a user to notice right away when a decent-sized object is placed in front of them and then taken away.

When the brain processes pulses, it can focus on the timing and spacing between them, making it easier to detect shifts in the environment or changes in sensory input. A pure frequency square wave, while providing a steady rhythm, can be harder for the brain to link to specific events unless it is directly related to a meaningful pattern or context.

Pure frequency square waves can be mentally demanding to decode, especially if they are used to represent complex information. The brain may struggle to differentiate between different frequencies or associate them with real-world objects or events. Pulses, on the other hand, can be perceived as discrete units of information that are more easily mapped to specific objects or changes in the environment. This reduces cognitive load and can enhance the user's ability to make sense of the information.

Pulses align better with how the brain encodes sensory information. Neurons often fire in bursts or patterns, and pulses mimic this biological mechanism of event detection. The brain is more sensitive to these bursts or patterns of activity than to continuous signals, making pulses a natural way to represent changes in the environment.

This is really the aim of this project, to **completely remove conscious interpretation from the input received** and hand it to the more primal regions of the brain for processing.

**Depth Representation:**

The system uses variations in pulse intensity or frequency shifts to represent the depth of objects in the environment. For example, objects that are closer might be represented with stronger or more frequent pulses, while more distant objects are conveyed with weaker pulses or less frequent intervals.

**Monophonic Output:**

The system is optimized for mono-sound users, with the pulses being rendered as a singular stream of auditory feedback. This ensures that the sound output can be processed and understood by individuals who may only have hearing in one ear.

**Edge and Feature Detection:**

As the system identifies the contours of objects, the resulting pulses can convey not only the object’s presence but also its outline, allowing users to perceive shapes and movements.

**[Training]**

Now that I've begun serious testing, I will document the findings here.

**Day 1** - Time spent: 20 minutes
**50x50 - On a surface with no texture**
* This tool has such high-fidelity output, that highly textured surfaces create a tremendous amount of pulse-noise.

- It is possible for a user to clearly tell when an object had been placed, multiple objects were not tested.
  
- Location of object can be determined, sometimes the camera would have to be moved around to determine where it was relative to the camera.
* It seems the 'size' of the pulse signature of the object is larger when it is placed closer to the user, this is what I was hoping for when trying to virtualize depth, it shows there is a metric for object location based on size the brain is using.
  
- Somehow, position of the object relative to the user can be determined; but could this be a coincidence? The surface size (a table) was not huge.
* User described having a 'knowing' of where the object was most of the time, they seemed to know the general position of the object relative to the camera, but could not explain how they knew. The only thing that confused them was a crack in the table, but once they knew the location of the crack it was a non-issue.

Yet, it was registered as a 'second object' by the algorithm of the tool, it is something i want to note.

I will continue this to have the user train at 50x50 for 1 week before introducing a second object, to see if the user can perceive a difference in the pulse signature of it.

For now, I want to verify that they can somehow locate where the object is, this should not really be possible with just 20 minutes of dedicated training so I'm chalking it up to a coincidence, but we'll see.
