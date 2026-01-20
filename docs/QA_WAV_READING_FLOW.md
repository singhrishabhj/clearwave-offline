# Q&A – WAV File Reading Flow

This document explains how a WAV file is read in Java
from disk to usable audio samples.

---

## Q1: What happens when we read a WAV file?
When we read a WAV file:
1. Java reads the file from disk
2. Java checks the WAV header
3. Java understands the audio format
4. Java provides access to raw audio data

---

## Q2: Why can’t we read a WAV file like a text file?
A WAV file is a binary file, not text.

Text files contain readable characters.
WAV files contain raw numeric values.

Reading a WAV file as text would corrupt the data.

---

## Q3: What is the first Java object involved?
The first object is `AudioInputStream`.

It connects:
- The file on disk
- The audio format
- The raw audio bytes

---

## Q4: What kind of data do we get from AudioInputStream?
AudioInputStream provides:
- Raw audio data as bytes
- AudioFormat metadata

The bytes represent sound samples.

---

## Q5: Why do we get bytes instead of samples directly?
Computers store data in bytes.

Audio samples are encoded into bytes
based on the AudioFormat.

It is our responsibility to convert
bytes into meaningful numbers.

---

## Q6: What does “converting bytes to samples” mean?
Converting bytes to samples means:
- Grouping bytes correctly
- Respecting bit depth
- Respecting signed or unsigned values

This conversion allows us to process audio mathematically.

---

## Q7: Why don’t we reduce noise while reading?
AudioReader should only read data.

Noise reduction is a separate responsibility.

Mixing reading and processing would:
- Make code harder to test
- Break clean design principles

---

## Q8: What is the output of AudioReader?
AudioReader should return:
- Audio samples
- Audio format information

This allows other parts of the system
to process audio without caring about file details.

---

## Q9: How is this useful in interviews?
Interviewers often ask:
- How does data flow through your system?
- How do you separate responsibilities?

Being able to explain WAV reading step by step
shows strong foundational understanding.

