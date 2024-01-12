# SPEECH-EMOTION-RECOGNITION

## Introduction

The capacity to alter and create vocal sounds is one of the characteristics that distinguishes
humans from other living organisms. Pitch, timbre, loudness, and vocal tone are all characteristics of the human voice. It has been established that humans communicate their emotions by
altering distinct voice qualities during speech creation. As a result, deducing human emotions
using voice and speech analysis has a practical possibility and might perhaps be advantageous
for boosting human conversational and persuading abilities. Creating facial expression systems
based on speech has useful applications. When the system is used in actual applications, however, these advantages are partly overshadowed by the real-world background noise that impairs
speech-based emotion identification ability. Speech Emotion Recognition (SER) is one of the
most difficult challenges in the realm of speech signal analysis; it is a research topic that attempts
to infer emotion from speech data.

## Objectives

* To devolop and increase the efficiency of the human-machine interface is the main goal
for SER.
* We can try to empliment it in lie detectors to track a subject’s psychophysical condition.
* We can also find its applications in medicine and forensics departments.

## Methodology


![Web capture_12-1-2024_175757_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/e94ee948-21e9-4e32-8ae9-3c7727b7850f)
* The term ”chromagram” condenses all of the pitches within an audio file so that we may
comprehend how the audio files’ pitches are categorised.
* the structuring of the audio waveforms to provide precise, thorough representations of the
audio sources as a function of time delay
* spectral preprocessing is a method in which Alternate frequency domain representations
of a sound can be obtained by analysing it; these representations can then be reversed
and manipulated to create new sounds.
* A semitone has a frequency ratio of 2 to the power of(1/12) in terms of frequencies.
* One mainproperty of chroma features is that they capture harmonic and melodic characteristics of music, while being robust to changes in timbre
  
![Web capture_12-1-2024_175954_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/034372ad-5898-4756-8894-9a1101c47a09)

* Chroma features, which employ a 12-element spectral energy representation known as a
chroma vector, are an effective way to express music audio.
* where in each of the 12 bins represented a class of western music with 12 equal-tempered
pitches (semitone spacing)
* The majority of audio recordings have a frequency whose energy changes in relation to
time.
* To analyse the frequency energy at each time stamp, we utilize spectral contrast.
* Because it is difficult to measure energies, we utilise contrast to track changes in energy.

  ![Web capture_12-1-2024_18142_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/257d4d90-4ef0-46f5-8e0f-c507a92f38c6)

  * Frame blocking is the method of processing a speech signal in short time periods to extract
its distinctive properties in a more stable condition.
* Windowing is the process of splitting a spoken signal into segments of a specific length.
* The wrapping of mel frequency is usually carried out by a filterbank
* The estimated signal spectrum’s logarithm is calculated using the inverse Fourier transform to get the cepstrum.
* Cepstrum is used to convert the signals that had been combinrd by the convolution for
linear separation


  
