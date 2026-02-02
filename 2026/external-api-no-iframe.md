# External API without iframe

## Overview

Redesign the External API to allow direct integration without iframe isolation.

## Description

Currently, [Jitsi Meet's External API](https://jitsi.github.io/handbook/docs/dev-guide/dev-guide-iframe) requires
embedding the meeting in an iframe and communicating across the iframe boundary using postMessage. While this provides
security isolation, it also adds complexity and overhead.

This project aims to create an alternative integration method where Jitsi Meet can be embedded directly into a parent
page as a JavaScript module/component, without requiring an iframe. This would allow for tighter integration, direct
API access, and potentially better performance while maintaining security through other means.

## Expected outcomes

* New API that allows direct instantiation of Jitsi Meet without iframe.
* Maintain feature parity with current iframe-based External API.
* Sample applications demonstrating the new integration approach.

## Skills / Technologies

JavaScript, TypeScript, React

## Possible mentors

Hristo Terezov, Damyan Minkov

## Expected project size

Medium (175 hrs)

## Difficulty

Medium

