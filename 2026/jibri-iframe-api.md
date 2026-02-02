# Rewrite Jibri to use iframe API

## Overview

Modernize Jibri's architecture by migrating to the External API for better control and maintainability.

## Description

[Jibri] (Jitsi Broadcasting Infrastructure) is responsible for recording and live
streaming Jitsi Meet conferences. Currently, Jibri runs a headless Chrome/Chromium instance that loads Jitsi Meet
directly and captures the audio/video output.

This project aims to rewrite Jibri to use the [External API](https://jitsi.github.io/handbook/docs/dev-guide/dev-guide-iframe)
instead of direct page loading. This architectural change would provide better control over the meeting, cleaner
separation of concerns, easier maintainability, and access to External API features for enhanced recording capabilities.

## Expected outcomes

* Rewrite Jibri to use iframe API instead of direct page loading
* Maintain feature parity with current recording and streaming capabilities
* Updated documentation and deployment guides

## Skills / Technologies

Kotlin, Java, Selenium WebDriver, JavaScript

## Possible mentors

Mihaela Dumitru, Boris Grozev

## Expected project size

Medium (175 hours)

## Difficulty

Medium

