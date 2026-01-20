# Q&A – Java Sound API (Beginner)

This document explains how Java works with audio files
in very simple terms.

---

## Q1: What is Java Sound API?
Java Sound API is a built-in Java library that allows programs
to work with audio.

It supports:
- Reading audio files
- Writing audio files
- Playing sound
- Capturing sound

---

## Q2: Why are we using Java Sound API?
We use Java Sound API because:
- It is built into Java (no extra dependency)
- It supports WAV files
- It is good enough for learning audio basics
- It is commonly used in interviews and projects

---

## Q3: What is AudioSystem?
AudioSystem is a utility class provided by Java.

It acts as an entry point to:
- Load audio files
- Get audio input streams
- Access audio devices

Think of it as a factory for audio-related objects.

---

## Q4: What is AudioInputStream?
AudioInputStream represents an audio file as a stream of data.

It allows us to:
- Read audio data gradually
- Access audio format information
- Convert raw bytes into samples

It is similar to InputStream, but for audio.

---

## Q5: What is AudioFormat?
AudioFormat describes how audio data should be interpreted.

It contains:
- Sample rate
- Number of channels
- Bit depth
- Encoding type

Without AudioFormat, Java would not know
how to read the audio bytes correctly.

---

## Q6: Why do we need AudioFormat?
AudioFormat tells Java:
- How many bytes represent one sample
- Whether audio is mono or stereo
- How fast samples occur

It acts like a decoder guide for audio data.

---

## Q7: What is PCM?
PCM (Pulse Code Modulation) is a way of representing audio
as raw numeric values.

Most WAV files use PCM encoding.

PCM is simple, uncompressed, and ideal for learning.

---

## Q8: Why is Java Sound API considered low-level?
Java Sound API works close to raw audio data.

It does not:
- Automatically reduce noise
- Automatically improve quality

This is good for learning because
we can control and understand everything.

---

## Q9: How is this useful in interviews?
Interviewers want to see:
- That you understand APIs you use
- That you know why you chose a tool
- That you can explain data flow clearly

Knowing Java Sound API basics
shows strong core Java understanding.

