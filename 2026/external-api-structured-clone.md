# External API with non-serialized postMessages

## Overview

Optimize the External API by migrating from serialized to structured clone postMessages.

## Description

The current external API relies on JSON serialization for all postMessage communication between the parent page and the Jitsi Meet iframe. This approach has performance overhead and limitations on the types of data that can be transferred.

Modern browsers support structured cloning and transferable objects in postMessage, which allows for more efficient
data transfer without serialization. This project aims to migrate the External API to use these capabilities,
improving performance and enabling support for richer data types.

## Expected outcomes

* Migration of External API to use structured cloning instead of JSON serialization.
* Support for transferable objects (ArrayBuffers, ImageData, etc.) where applicable.
* Backward compatibility layer for existing integrations.
* Updated API documentation with examples of new capabilities.
* Test coverage for complex data type transfers.

## Skills / Technologies

JavaScript, TypeScript, Web APIs, postMessage, Structured Clone Algorithm

## Possible mentors

Saúl Ibarra Corretgé

## Expected project size

Medium (175 hours)

## Difficulty

Medium

