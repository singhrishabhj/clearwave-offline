# Audio Basics for Beginners

This document explains basic audio concepts in simple terms.
No prior knowledge of audio processing is required.

---

## What is Digital Audio?
Digital audio is sound represented as numbers.
A continuous sound wave is converted into discrete numerical values
that a computer can store and process.

---

## What is a Sample?
A sample is a single numeric value that represents the loudness
(amplitude) of sound at a specific moment in time.

An audio file is essentially a long list of such samples.

---

## What is Amplitude?
Amplitude represents how loud the sound is.
- High amplitude → loud sound
- Low amplitude → soft sound

Silence does not mean “no value”; it usually means very small values.

---

## What is Noise?
Noise is any unwanted sound that is mixed with the actual signal.
Examples:
- Background hiss
- Electrical hum
- Fan or wind noise

Noise usually appears as small random variations in audio samples.

---

## Why Noise Reduction is Hard
Noise often overlaps with useful sound (like human voice).
Removing too much noise can also remove useful information.

This is why noise reduction always involves trade-offs.

