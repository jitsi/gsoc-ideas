# Audio Switchboard API

## Overview

Design and implement a protocol and an API to allow participants in a [Jitsi Meet]() conference to use
different audio channels.

## Description

[Jitsi Meet]() clients use a very flexible [constraints](https://github.com/jitsi/jitsi-videobridge/blob/master/doc/allocation.md) API
to select which video streams in a conference they want to received. However, audio is not configurable: endpoints always receive
all audio streams (optionally filtered by loudness).

The goal of this project is to build the lower level functionality to allow endpoints more control over
what they receive. This would allow various exciting features to be implemented on top of it: live translation layers,
lightweight breakout rooms, whispering, etc.

## Expected outcomes
* A protocol between a client and [Jitsi Videobridge]() for publish/subscribe audio channels
* Audio filtering in Jitsi Videobridge based on channels
* \[Optional: A javascript API that allows clients to change the audio channels they receive/send\]

## Skills / Technologies

Kotlin, Java, JavaScript

## Possible mentors
Boris Grozev, Saúl Ibarra Corretgé, Jonathan Lennox

## Expected project size

Large (350 hours)

## Difficulty

Hard

[Jitsi Videobridge](https://github.com/jitsi/jitsi-videobridge/)
[Jitsi Meet](https://github.com/jitsi/jitsi-meet/)
