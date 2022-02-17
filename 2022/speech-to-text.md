# Speech-to-text with publicly available deep learning models

## Prerequisites
Prior knowledge in these areas will be an advantage for this project, but none of them
are strictly necessary:

* Git
* Java
* Basics of HTTP
* Python, C++ or even another language depending on the open-source speech-to-text project 

## Previous work
Previous GSoC projects have experimented with the implementation of
speech-to-text API’s in [Jitsi Meet](https://github.com/jitsi/jitsi-meet), such
as Google’s, IBM’s and the open-source tool CMUSphinx. The current
speech-to-text implementation uses the paid, proprietary Google speech-to-text
API. It would be nice to offer a free, privacy-friendly alternative.

Although this project is closely related to deep learning, it is very unlikely
to involve training our own model. It takes a huge amount of computational
power and time to train (state-of-the-art) deep neural networks. We do not have
the resources (GPU nor data) for training these networks. The project should
involve finding pre-trained models freely available to the public and do the
required engineering to make these models serve transcriptions in a Jitsi Meet
conference call.

There are some open-source libraries which could fit our needs as a starting point:

* https://huggingface.co/models?pipeline_tag=automatic-speech-recognition&sort=downloads

## The project:
The current implementation of speech-to-text is based on
[Jigasi](https://github.com/jitsi/jigasi). Jigasi is able to join a Jitsi Meet
conference call as a “robotic guest”. It will get access to all the audio of
the participants and forward it to a speech-to-text engine. The speech-to-text
engine will do inference and return the transcription to Jigasi. This
transcription is then sent back to the conference call by Jigasi, and displayed in
the participants' user interface. The inference speed of the speech-to-text
model is important, as we would like the delay to be as small as possible. The
open-source model should most likely run on a different server, which Jigasi
can request. The main engineering tasks will therefore be:

* Implement/find a web server wrapping the open-source speech-to-text model
* Implement the communication between the server and Jigasi

## Pro tips for your application
Your GSoC application would be super awesome if you show that you managed to
record a small audio clip of yourself and have an open-source speech-to-text
toolkit transcribe it! It would be cool if you find other useful public models
which could serve our needs. 

If you have any questions, feel free to [create an issue](https://github.com/jitsi/gsoc-ideas/issues/new)!

## Mentors

@nikvaessen
