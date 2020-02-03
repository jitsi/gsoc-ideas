# Chromecast or AirPlay screen sharing in Jitsi Spot

## Prerequisites

* Git
* Javascript
* WebRTC
* iOS/Android

## The project:

[Spot] is part of the Jitsi ecosystem for conference room integration. It runs
on the main TV/screen in a conference room and is controlled either through
a tablet or from a laptop by opening the webpage dedicated for the remote
control functionality.

Spot screen displays a list of upcoming calendar events and allows to join
a conference if there's a valid Jitsi Meet URL in the event's description. Once
Spot joins a Jitsi Meet conference it's possible to stream your laptop's screen
as if it was sent directly by the Spot conference participant.

The idea is to make Spot participant a valid Chromecast or AirPlay streaming
destination and send the casted stream into a Jitsi Meet conference. It's okay
to choose either Chromecast or AirPlay, but doing both would be great.

## Pro tips for your application

The main and the most important part of the application should be a high level
concept on how Chromecast/AirPlay can be integrated with [Spot]. Being able to
run [Spot] in your local dev environment will be a plus.

If you have any questions, feel free to [create an issue](https://github.com/jitsi/gsoc-ideas/issues/new)!

## Mentors

@paweldomas

[Spot]: https://github.com/jitsi/jitsi-meet-spot
