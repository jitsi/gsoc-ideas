### Speech-to-text with publicly available deep learning models

Previous GSoC projects have experimented with the implementation of speech-to-text API’s in Jitsi Meet, such as Google’s, IBM’s and the open-source tool CMUSphinx. The current speech-to-text implementation uses the paid, proprietary Google speech-to-text API. We think it would be nice to offer a free, privacy-friendly alternative, albeit with worse accuracy. 

Although this project is closely related to deep learning, it is very unlikely to involve training our own model. It takes a huge amount of computational power and time to train (state-of-the-art) deep neural networks. We do not have the resources (GPU nor data) for training these networks. The project should involve finding pre-trained models freely available to the public and do the required engineering to make these models serve transcriptions in a Jitsi Meet conference call. 

There are some open-source libraries which could fit our needs as a starting point:

* https://github.com/facebookresearch/wav2letter 
* https://github.com/mozilla/DeepSpeech
* https://github.com/PaddlePaddle/DeepSpeech#released-models 

General idea of the project:

The current implementation of speech-to-text is based on Jigasi (https://github.com/jitsi/jigasi). Jigasi is able to join a Jitsi Meet conference call as a “robotic guest”. It will get access to all the audio of the participants and forward it to a speech-to-text engine. The speech-to-text engine will do inference and return the transcription to Jigasi. This transcription is then sent back to the conference call by Jigasi, and the participants will be able to see it. The inference speed of the speech-to-text model is important, as we would like the delay to be as small as possible. The open-source model should most likely run on a different server, which Jigasi can request. The main engineer tasks will therefore be:

* Implement/find a web server wrapping the open-source speech-to-text model
* Implement the communication between the server and Jigasi

For you to complete this project, we think you must have: 
* motivation to learn things you do not yet know!
show us you’ve written code

What you will definitely know at the end of the summer and would help your chances of being accepted:
* Git
* Java (1.8) for tasks involving back-end
* Basics of HTTP
* Python, C++ or even another language depending on the open-source speech-to-text project 

Your GSoC application would be super awesome if you show that you managed to record a small audio clip of yourself and have an open-source speech-to-text toolkit transcribe it! It would be cool if you find other useful public models which could serve our needs. 

If you have any questions, feel free to create an issue!



