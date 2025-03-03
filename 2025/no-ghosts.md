# Removing "ghost" participants on reconnections

## Overview

Detect reconnections due to failure and kick out the "ghost" participant from the previous connection.

## Description

Jitsi Meet is subject to network connection problems, variance. A particularly annoying problem happens when a user reconnects
after a connection failure. A new tile will appear, but the previous one, for the (now dead) connection will remain there for
1-3 minutes, until the connection is presumed fully dead and it gets kicked. We refer to these user tiles as "ghosts".
This situation can be optimized if we detect a user is reconnecting and can automatically replace the ghost tile with
the new real one.

## Expected outcomes

* TypeScript code handling this problem

## Skills / Technologies

JavaScript, TypeScript

## Possible mentors

Saúl Ibarra Corretgé, Damyan Minkov

## Expected project size

Medium (175 hours)

## Difficulty

Medium

