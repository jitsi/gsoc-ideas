# External API Structured Clone - First PR Template Pack

This page gives you copy-paste friendly text for your first GSoC PRs on the External API structured clone project.

## PR 1: Benchmark harness

Suggested title:

GSoC: feat(external-api): add benchmark harness for JSON vs structured clone messaging

Suggested branch name:

gsoc26/external-api-structured-clone-benchmark

Suggested PR description:

### Summary

This PR adds a benchmark harness to compare message handling performance between:

- JSON serialize and parse flow
- structured clone flow

The goal is to establish a reproducible baseline before migration work.

### Why

The External API currently relies on JSON serialization for iframe communication. Structured clone can reduce overhead and support richer payloads, but we need baseline numbers before making behavior changes.

### Changes in this PR

- Adds benchmark utility for representative message payloads.
- Covers small, medium, and large payload classes.
- Prints timing summaries in a consistent format for local comparison.
- Adds short documentation for running benchmarks locally.

### Validation

- Ran benchmark locally multiple times and confirmed stable output format.
- Verified benchmark includes both JSON and structured clone paths.
- Confirmed no runtime behavior changes in production message handling.

### Out of scope

- No migration of production message handling in this PR.
- No API shape changes.

---

## PR 2: Typed array round-trip tests

Suggested title:

GSoC: test(external-api): add structured clone round-trip tests for typed arrays

Suggested branch name:

gsoc26/external-api-structured-clone-typed-array-tests

Suggested PR description:

### Summary

This PR adds tests that verify structured clone message paths correctly round-trip binary-friendly data types.

### Why

JSON serialization is not suitable for all binary payloads. We need reliable coverage for richer data types before enabling structured clone paths broadly.

### Changes in this PR

- Adds test cases for typed array payloads.
- Verifies data integrity after parent to iframe and iframe to parent message round-trips.
- Adds negative tests for unsupported payload shapes where applicable.

### Validation

- Ran the relevant test suite locally.
- Verified typed array contents and lengths are preserved after round-trip.
- Confirmed existing JSON-based tests continue to pass.

### Out of scope

- No transferable ownership optimization in this PR.
- No backward compatibility removal.

---

## PR 3: Backward compatibility fallback tests

Suggested title:

GSoC: test(external-api): cover fallback behavior for legacy serialized payloads

Suggested branch name:

gsoc26/external-api-structured-clone-fallback-tests

Suggested PR description:

### Summary

This PR adds compatibility tests to ensure legacy integrations that still send serialized payloads continue to work.

### Why

Migration must be safe for existing users. Compatibility behavior needs test coverage before rollout.

### Changes in this PR

- Adds tests for old serialized payload paths.
- Verifies fallback behavior when structured clone path is unavailable or disabled.
- Verifies event and command handling parity across old and new paths.

### Validation

- Ran the targeted test suite locally.
- Confirmed behavior parity for representative commands and events.
- Confirmed no regressions in existing integration tests.

### Out of scope

- No removal of legacy path.
- No deprecation switch in this PR.

---

## Universal checklist before opening each PR

- Title starts with GSoC:.
- One logical change only.
- Build and lint pass locally.
- Tests for changed behavior are included.
- PR description explains why, what changed, and what was validated.
- Reproduction or validation steps are clear.
- No unrelated refactors.

## Comment template for mentor discussion thread

I am planning a small contribution for the External API structured clone project.

Proposed PR scope:
- scope line 1
- scope line 2

Validation plan:
- validation line 1
- validation line 2

If this scope looks good, I will submit a focused PR with GSoC prefix and tests.
