# GSoC 2026 Contributor Starter Playbook

This playbook is for applicants who want a concrete path from "interested" to "credible contributor".

## Goal

Demonstrate three things early:

1. You can run the project locally and validate changes.
2. You can communicate clearly with mentors and the community.
3. You can deliver small, correct, reviewable pull requests.

## Week 1: Foundation

1. Pick one target idea from [README.md](README.md).
2. Read the contribution policy in [../CONTRIBUTING.md](../CONTRIBUTING.md).
3. Join existing GSoC 2026 discussions on the community forum.
4. Set up the target repository locally and run the baseline build/tests.

Deliverable:

* A short personal log with setup notes, blockers, and how you solved them.

## Week 2: First accepted contribution

1. Start with a small, real issue (docs/tests/low-risk bug fix) in your target codebase.
2. Open a PR with title prefix `GSoC:`.
3. Include reproduction or validation steps.
4. Keep the PR focused to one logical change.

Deliverable:

* First reviewable PR with clear before/after behavior.

## Week 3: Idea-aligned contribution

1. Build a small contribution directly related to your chosen 2026 idea.
2. Add tests for the changed behavior.
3. Share trade-offs and alternatives in the PR description.

Deliverable:

* Second PR that demonstrates domain understanding, not only coding.

## Week 4: Proposal draft from evidence

1. Turn your contributions into a milestone-based proposal.
2. Add measurable success criteria for each milestone.
3. List technical risks and fallback plans.

Deliverable:

* A proposal draft grounded in real repository work.

## PR checklist for applicants

* Title starts with `GSoC:`.
* Builds and lint checks pass.
* Includes reproduction/validation steps.
* Explains expected behavior and actual behavior.
* Avoids unrelated refactors.
* Keeps at most 3 active PRs at a time.

## Communication checklist

* Ask questions in existing GSoC 2026 forum threads.
* Avoid posting full proposal details publicly.
* Do not repeatedly ping mentors for review.
* Prefer precise technical questions over broad requests.

## Recommended first technical path

For many applicants, a strong medium-difficulty starting point is:

* [External API with non-serialized postMessages](external-api-structured-clone.md)

Why this path works:

* Clear scope and measurable impact.
* Strong TypeScript/Web API learning value.
* Good balance between complexity and reviewability.
