# Virtual Backgrounds, take 2

## Overview

Improve the virtual backgrounds in Jitsi Meet so they perform as good as possible.

## Description

The current implementation for virtual backgrounds relies on a WASM build of Tensor Flow Lite (tflite) which predates
the release of MediaPipe.

The project consists of migrating away from this package to MediaPipe and making performance oriented changes to
make sure the quality is a good as it can be. A non exhaustive list of potential improvements: use WebGL for rendering,
use requestVideoFrameCallback for driving the render, use insertable streams.

## Expected outcomes

* A do-over of the feature, with higher quality than today

## Skills / Technologies

JavaScript, TypeScript

## Possible mentors

Saúl Ibarra Corretgé

## Expected project size

Medium (175 hours)

## Difficulty

Medium
