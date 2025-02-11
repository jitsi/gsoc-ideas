# Jitsi Videobridge JavaScript client (jvb-js)

## Overview

JavaScript library for communicating with the [Jitsi Videobridge](https://github.com/jitsi/jitsi-videobridge).

## Description

The JVB is the heart of Jitsi Meet. It's the entity responsible for video routing.

Jitsi Meet uses many more components than the JVB, connecting them via XMPP. This setup may not be desirable for everyone
so a low level library that can connect to the JVB directly would give developers the ultimate flexibility to use our
video router, without having to buy into the entire ecosystem.

## Expected outcomes

* TypeScript library which can communicate with the JVB and negotiate media sessions
* Sample "meetings app" using the previously built library and socket.io for signalling

## Skills / Technologies

JavaScript, TypeScript, socket.io (not strictly necessary)

## Possible mentors

Saúl Ibarra Corretgé, Boris Grozev

## Expected project size

Medium (175 hours) or Large (350 hours)

## Difficulty

Medium

