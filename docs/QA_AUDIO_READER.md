# Q&A – AudioReader and Audio Basics

This document contains beginner-level questions and answers
to understand how audio files work and how AudioReader is designed.

---

## Q1: What is an audio file?
An audio file is a digital representation of sound.
Sound is stored as numbers that represent how loud the sound is
at different moments in time.

---

## Q2: What is a WAV file?
A WAV file is a common audio file format that stores sound
in an uncompressed form.

Because it is uncompressed:
- It is easier to read and process
- It preserves original sound quality
- It is commonly used in audio processing applications

---

## Q3: Why are we using WAV files in this project?
We use WAV files because:
- They are simple to understand
- Java has built-in support for WAV files
- There is no compression complexity
- They are ideal for learning audio processing basics

---

## Q4: What does a WAV file contain internally?
A WAV file contains:
1. Header information (metadata)
2. Audio format details (sample rate, channels, bit depth)
3. Raw audio data (samples)

The header tells the program how to interpret the audio data.

---

## Q5: What is a sample?
A sample is a single numeric value that represents
the loudness of sound at a specific moment.

An audio file is made of thousands or millions of samples.

---

## Q6: What is sample rate?
Sample rate tells how many samples are taken per second.

Example:
- 44,100 Hz means 44,100 samples per second

Higher sample rate:
- Better quality
- Larger file size

---

## Q7: What is a channel?
A channel represents an independent audio signal.

Examples:
- Mono → 1 channel
- Stereo → 2 channels (left and right)

---

## Q8: What is bit depth?
Bit depth defines how detailed each sample is.

Example:
- 16-bit audio allows more precision than 8-bit audio

Higher bit depth:
- Better dynamic range
- More accurate sound

---

## Q9: What is the responsibility of AudioReader?
AudioReader is responsible only for:
- Reading an audio file
- Extracting audio data
- Providing the data in a usable Java structure

It should NOT:
- Modify audio
- Reduce noise
- Write output files

---

## Q10: Why do we separate AudioReader from NoiseReducer?
Separating responsibilities:
- Makes code easier to understand
- Makes testing simpler
- Follows object-oriented design principles

This is called separation of concerns.

---

## Q11: What is separation of concerns?
Separation of concerns means:
Each class should handle one specific responsibility.

This makes systems:
- Easier to maintain
- Easier to test
- Easier to extend

---

## Q12: How is this useful in interviews?
Interviewers look for:
- Clear thinking
- Clean design
- Ability to explain fundamentals

Being able to explain AudioReader clearly
shows strong engineering basics.

---

## In what data type the audio samples are store and why ?
Audio samples are stored as float[] because floating-point values are easier to process mathematically during noise reduction and filtering.
