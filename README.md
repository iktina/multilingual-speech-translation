# multilingual-speech-translation

## Welcome

The service receives an audio file and uses it as an input for a trained models.

## What’s the point?

The service performs speech recognition using machine learning techniques.
The service receives the audio file in binary format and outputs the text string resulting from audio recognition. 

##  Model details:

The service receives an speech WAV audio file and uses it as an input to the Transformer model, based on a deep convolutional neural network trained in half-precision using a mixture of natural and synthetic data, and outputs the result of the speech sample recognition in form of a text sequence. The input audio file size is limited to 4Mb, in practice the optimal duration of the processed audio track should be no more than 90 seconds for 320 kbps audio.

## How does it work?

The user must provide the following inputs in order to start the service and get a response:

Inputs:

 -   `endpoint`: ?
 -   `method`: s2t.
 -   `input_path`: Path to '\*.txt' file containing JSON representation of input argument 'file@data' and its value - path to '\*.wav' input audio file.

Example of input file content:

```
{"file@data": "samples/sample.wav"}
```

## What to expect from this service?

Input audio:
samples/sample.wav

Response:
`text: "after a time she heard a little pattering of feet in the distance and she hastily dried her eyes to see what was coming"`
