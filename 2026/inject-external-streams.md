# Inject external streams via iframe API

## Overview

Enable injection of external MediaStreams into Jitsi Meet conferences through the External API.

## Description

Currently, Jitsi Meet's external API allows control over various conference aspects, but doesn't provide a way to inject custom MediaStreams as video or audio sources.

This project aims to extend the External API to allow parent applications to inject their own MediaStreams into the
conference. This would enable use cases such as playing pre-recorded video, streaming from canvas elements, custom
audio/video processing pipelines, virtual cameras, or integrating external video sources.

## Expected outcomes

* External API methods to inject custom video and audio MediaStreams
* Handle stream lifecycle (starting, stopping, replacing)
* Documentation and examples for common use cases (canvas streaming, video playback, etc.)

## Skills / Technologies

JavaScript, TypeScript, WebRTC

## Possible mentors

Jaya Allamsetty, Saúl Ibarra Corretgé 

## Expected project size

Medium (175 hours)

## Difficulty

Medium

