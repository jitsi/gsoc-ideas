# Scalable Deployments

## Overview

Create templates for running a [Jitsi Meet](https://github.com/jitsi/jitsi-meet/) system in a scalable and geo-located way.

## Description

The [docker-jitsi-meet](https://github.com/jitsi/docker-jitsi-meet) project
allows one to run the various Jitsi components as docker images, and even run
an entire system using docker-compose. Adding high-availability, geo-located
servers, or (auto)scaling the number of machines can be accomplished in a
number of ways, and it's usually dependent on the environment.

We aim to provide a set of sample ways to achieve these goals
(HA/geo-location/scaling) for some of the common cloud environments (OCI, AWS,
etc).

The project will involve understanding the Jitsi architecture and how it fits
within a cloud environment, making changes to the docker images to expose extra functionality if needed,
and documenting the process.

## Expected outcomes
* Updates to docker-jitsi-meet exposing more configuration options
* A set of sample documents detailing how to setup Jitsi for HA/geo-location/scaling.

## Skills / Technologies

Docker, cloud, AWS, OCI, Azure

## Possible mentors
Boris Grozev, Saúl Ibarra Corretgé

## Expected project size

Medium (175 hours) or Large (350 hours)

## Difficulty

Medium
