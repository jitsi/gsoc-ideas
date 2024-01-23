# Jiconop for WebSockets

## Overview

Optimize the initial connection time to a [Jitsi Meet](https://github.com/jitsi/jitsi-meet/) conference by introducing a 
proxy between clients and the [prosody](https://prosody.im) XMPP server.

## Description

Clients in a Jitsi Meet conference use an [XMPP WebSocket](https://datatracker.ietf.org/doc/html/rfc7395) to connect to a [prosody](https://prosody.im) XMPP server.
The initial connection requires multiple round-trips and can be slow in networks with higher delay. This project aims to
optimize the initial connection time by introducing a proxy between cliens and prosody, which
batches some of the exchanges.

The [jiconop](github.com/jitsi/jiconop) project has the same conceptual design, but works with BOSH instead of WebSockets,
 so the implementation details are completely different.


## Expected outcomes
* A WebSocket proxy which sits between [jitsi-meet](https://github.com/jitsi/jitsi-meet/) clients and the prosody XMPP server
* Changes to the [strophejs](https://strophe.im/strophejs/) library to support the protocol changes required

## Skills / Technologies

XMPP, HTTP/WebSockets, JavaScript, Lua

## Possible mentors
Boris Grozev, Damian Minkov

## Expected project size

Medium (175 hours) or Large (350 hours)

## Difficulty

Hard

