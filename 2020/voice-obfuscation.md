# Voice Obfuscation (a.k.a voice anonymization)

## Prerequisites
Prior knowledge in these areas will be an advantage for this project, but none of them
are strictly necessary:

* Git
* JavaScript
* WebRTC
* Audio processing

## Goals
To add a feature to [Jitsi Meet](https://github.com/jitsi/jitsi-meet) that
modifies the audio before it is sent to the conference, helping users to stay
anonymous.

## Implementation
The implementation would consist of two parts.

1. Develop a generic framework that allows processing the audio stream before it is encoded.
2. Integrate an existing library for voice obfuscation and add the necessary UI elements to enable the feature.

## Pro tips for your application
Can you find any suitable open-source libraries? Can you find an appropriate
place in [lib-jitsi-meet](https://github.com/jitsi/lib-jitsi-meet) where your
code can fit? Best of all, can you provide a proof-of-concept?

If you have any questions, feel free to [create an issue](https://github.com/jitsi/gsoc-ideas/issues/new)!

## Potential mentors

@bgrozev
