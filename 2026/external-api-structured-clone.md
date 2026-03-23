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

## Suggested execution plan (for applicants)

The steps below are a practical path to begin contributing and reduce risk.

### Phase 0: Discovery and baseline

* Locate all parent <-> iframe API message paths and classify message types.
* Measure baseline serialization overhead for small and large payloads.
* Document browser compatibility assumptions for structured clone and transferables.

### Phase 1: Core migration

* Replace JSON serialization with structured clone where behavior is equivalent.
* Add explicit message schema validation for high-risk commands/events.
* Keep a compatibility path for legacy integrations that still expect serialized payloads.

### Phase 2: Transferable objects

* Introduce transferables only where they provide real benefit and low complexity.
* Cover ArrayBuffer and similar binary-heavy paths first.
* Validate object lifetime rules after transfer to avoid use-after-transfer bugs.

### Phase 3: Validation and rollout

* Add integration tests for mixed old/new client behavior.
* Add docs and examples showing structured clone payloads.
* Add rollout notes and guardrails for safe incremental adoption.

## First PR ideas

* Add a benchmark harness for comparing JSON serialization vs structured clone in representative API calls.
* Add tests that verify non-JSON-safe data (for example typed arrays) can round-trip correctly.
* Add compatibility tests for fallback behavior when integrations send old payload formats.

## Ready-to-use PR draft

Use this template pack to submit your first contributions quickly:

* [External API Structured Clone - First PR Template Pack](external-api-structured-clone-pr-template.md)

## Success metrics

* Lower average message processing time on large payload paths.
* No regressions in existing External API integrations.
* Green test coverage for structured clone and fallback paths.

