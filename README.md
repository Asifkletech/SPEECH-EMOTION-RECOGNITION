# SPEECH-EMOTION-RECOGNITION

## Introduction

The capacity to alter and create vocal sounds is one of the characteristics that distinguishes
humans from other living organisms. Pitch, timbre, loudness, and vocal tone are all characteristics of the human voice. It has been established that humans communicate their emotions by
altering distinct voice qualities during speech creation. As a result, deducing human emotions
using voice and speech analysis has a practical possibility and might perhaps be advantageous
for boosting human conversational and persuading abilities. Creating facial expression systems
based on speech has useful applications. When the system is used in actual applications, however, these advantages are partly overshadowed by the real-world background noise that impairs
speech-based emotion identification ability. Speech Emotion Recognition (SER) is one of the
most difficult challenges in the realm of speech signal analysis; it is a research topic that attempts
to infer emotion from speech data.

## Objectives

* To develop and increase the efficiency of the human-machine interface is the main goal
for SER.
* We can try to implement it in lie detectors to track a subject’s psychophysical condition.
* We can also find its applications in medicine and forensics departments.
* We can use it in Robotics to understand human emotions through voice
* It can be deployed in Automotive Vehicles

## Methodology
# Chroma

![Web capture_12-1-2024_175757_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/e94ee948-21e9-4e32-8ae9-3c7727b7850f)
* The term ”chromagram” condenses all of the pitches within an audio file so that we may
comprehend how the audio files’ pitches are categorized.
* the structuring of the audio waveforms to provide precise, thorough representations of the
audio sources as a function of time delay
* spectral preprocessing is a method in which Alternate frequency domain representations
of a sound can be obtained by analyzing it; these representations can then be reversed
and manipulated to create new sounds.
* A semitone has a frequency ratio of 2 to the power of(1/12) in terms of frequencies.
* One main property of chroma features is that they capture harmonic and melodic characteristics of music, while being robust to changes in timbre

  # Contrast 
  
![Web capture_12-1-2024_175954_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/034372ad-5898-4756-8894-9a1101c47a09)

* Chroma features, which employ a 12-element spectral energy representation known as a
chroma vector, are an effective way to express music audio.
* wherein each of the 12 bins represented a class of Western music with 12 equal-tempered
pitches (semitone spacing)
* The majority of audio recordings have a frequency whose energy changes concerning
time.
* To analyze the frequency energy at each timestamp, we utilize spectral contrast.
* Because it is difficult to measure energies, we utilize contrast to track changes in energy.

  # MFCC

  ![Web capture_12-1-2024_18142_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/257d4d90-4ef0-46f5-8e0f-c507a92f38c6)

  * Frame blocking is the method of processing a speech signal in short periods to extract
its distinctive properties in a more stable condition.
* Windowing is the process of splitting a spoken signal into segments of a specific length.
* The wrapping of Mel frequency is usually carried out by a filterbank
* The estimated signal spectrum’s logarithm is calculated using the inverse Fourier transform to get the cepstrum.
* Cepstrum is used to convert the signals that had been combined by the convolution for
linear separation

# LSTM(Long Short Term Memory)

The capability of each unit’s knowledge to be learned, unlearned, or retained in a specific order is
thanks to a cell state, three gates, and an LSTM module. Through the restriction of the number
of linear interactions, the cell state in LSTM enables the uninterrupted flow of information
between the units. Three layers make up the LSTM network: an input layer, a single hidden
layer, and a typical feedforward output layer

![Web capture_12-1-2024_18652_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/bce5a6d0-a2c1-4451-bcff-2a6a6981b8a9)

The output of LSTM is particularly dependent on three things:
* cell state - the most recent long-term memory of the network
*  hidden state - the output from the preceding moment
* The input information for this time step

  # Why work with LSTM

  The vanishing gradient problem with RNNs (Recurrent Neural Networks) was resolved by the
development of the LSTM network. In contrast to more conventional feedforward neural networks, they have feedback connections. To facilitate the processing of new data points, the
LSTM saves pertinent information from earlier data points in the sequence. As Consequently,
it excels at processing voice, text, and general time series.

We’ll try to explain the LSTM model by using an example. Imagine that we’re
attempting to forecast monthly ice cream sales. These vary considerably according on the
month of the year. This pattern, which repeats itself every 12 cycles, can be learned by an LSTM
network and is lowest in December and highest in June. It overcomes the problem of long-term
dependency that other models have by not just using the prior forecast but also keeping in mind
a wider context. This is a pretty simple example and as the pattern is separated by much longer
periods, LSTMs become beneficial.

# DATASET

We have used the dataset known as RAVDESS(The Ryerson Audio-Visual Database of Emotional
Speech and Song). link(https://zenodo.org/record/1188976.Y1EP53ZBxPZ)
* There are a total of 7356 files in the RAVDESS(Ryerson Audio-Visual Database of Emotional Speech and Song )(total size: 24.8 GB).
* The dataset has a total of 24 qualified actors which there are 12 females and 12 males
 , each of whom reads two lexical and grammatical related sentences with an American
accent.
* Both speech and music contain a range of emotions, including those associated with serenity, happiness, sadness, anger, fear, surprise, and disgust. There are two emotional intensity levels (normal and strong)
* Three modalities—Audio only (16bit, 48kHz.wav), Audio video (720p H.264, AAC 48kHz,.mp4),
and Video only—are offered for all situations (no sound).In which we are only going to
use the audio only as a database

# IMPLEMENTATION

![Web capture_12-1-2024_181327_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/2d097660-d66c-41a3-b275-f73f58eb934d)

With a total of 2900 audio recordings, the RAVDESS dataset with audio only was
utilized. We used that as an input, as shown in Fig. 6.1. In the procedure, we used contrast,
chroma, and MFCCs as the three primary elements to detect emotions. A total of 40 MFCCs,
12 contrast and 7 chroma characteristics have been collected. Next, using an Excel spreadsheet,
we properly organized the features into rows and columns before sending it to the LSTM model
. As shown in the following block diagram we have used an input layer, 2 RELU layers, and a
single softmax layer. The abbreviation for RELU is a rectified linear unit the advantage of this
unit is that it does not activate all the neurons at a single time. Softmax it is used to represent
the output as 0 or 1.

![Web capture_12-1-2024_18179_](https://github.com/Asifkletech/SPEECH-EMOTION-RECOGNITION/assets/151855456/6ff36ce8-8af6-4de4-9c59-d1ddafbe713b)


# CONCLUSION

In this paper, we have used the LSTM model and worked with the features as mentioned above in
the paper(chroma,contrast,MFCCs).We are using the LSTM model because it can resolve the
the issue regarding RNNs(vanishing gradient problem), is also that they have feedback network
as LSTM preserves relevant data from earlier data points in the sequence to aid in processing
new data points. The overall accuracy that we can get by using this LSTM model 80
percentage

# FUTURE SCOPE

It can be used in AI or robots to make them understand human emotions and act according
to that of the human's mood. For example, when a human is in a bad mood, the robot must try
to calm the human down instead of making him more irate. Customer service representatives
might find it helpful to know the mood in which their customers are and give an appropriate
answer by deciding their mood.


  
