# How to Contribute

We greatly appreciate your willingness to contribute. Before you start, please read this guide.

## Reporting Issues and Asking Questions

Please discuss issues first in the community forum. Once confirmed, open an issue in the appropriate GitHub project repository.

- Report bugs, request features, or ask for help.
- When opening an issue, provide as much detail as possible.
- Ask general and implementation-specific questions in the community forum.

## Bug Reports and Other Issues

For bugs, please include:

1. Detailed version information for Jitsi Meet, Jicofo, and JVB.
2. A clear description of the issue.
3. Reproduction steps.
4. Expected behavior.
5. Actual behavior, including error messages.

## Feature Requests

If you have a new idea or improvement request, include:

1. Feature description and desired functionality.
2. Examples from other apps (if relevant).
3. Why the feature is important.
4. Potential implementation challenges.
5. Any additional preferences or details.

## Code Contributions

Start by checking open issues in the relevant tracker (for example, Jitsi Meet's issue tracker).

If you discovered a bug or have a feature request and know how to fix it, review the Developer Guide to set up your environment and begin work.

## Contributor License Agreement (CLA)

Jitsi projects are released under Apache License 2.0, and the copyright holder and principal creator is 8x8.

To accept your contribution, you must sign the Apache-based contributor license agreement as an individual or as a corporation. If you cannot accept the CLA terms, we cannot accept the contribution.

## Creating Pull Requests

1. Fork the repository to your GitHub account.
2. Create a descriptive branch from `master`.
3. Make one logical change per pull request.
4. Keep commit history clean and concise (squash if needed).
5. Rebase onto the latest `master` before submitting.
6. Never merge `master` into your branch; always rebase.

## Commit Messages

Jitsi projects follow Conventional Commits with a mandatory scope.

- Preferred: `feat(feature-name): add some functionality`
- Not preferred: `feat: add some functionality`

Supported commit types include:

- `build`
- `chore`
- `ci`
- `docs`
- `feat`
- `fix`
- `perf`
- `refactor`
- `revert`
- `style`
- `test`

Scope naming can vary by project and subsystem.

- In Jitsi Meet, a scope can be a feature path such as `react/features/<feature>`.
- In lib-jitsi-meet, a scope can be a module path such as `modules/<module>`.

Use your judgment and review commit history when unsure.

### For 8x8 Employees

Do not link internal resources such as Jira issues. This is an open source project.

## Coding Style

### Comments

- Source code comments are required.
- Auto-generated documentation comments (for tools like JSDoc, Javadoc, Doxygen) should follow tool conventions.
- Non-generated comments are strongly encouraged when they improve understanding.
- Write comments as proper English sentences with capitalization and punctuation.

### Duplication

- Avoid copy-pasting source code.
- Prefer reuse, but avoid introducing poor abstractions for minimal reuse.

### Naming

- Use one consistent name for an abstraction across the project(s).
- For example, a `JitsiConnection` instance should be named `connection` or `jitsiConnection`, not `client`.
- Keep class names and file names aligned (for example, class `ReducerRegistry` in `ReducerRegistry.js`).
- Use uppercase with underscores for global constants, for example `BACKGROUND_COLOR`.
- Leading underscore in names indicates non-public/internal members.

## TypeScript

### Feature Layout

When adding a new feature, use this structure:

```text
react/features/sample/
|- actionTypes.ts
|- actions.ts
|- components/
|  |- AnotherComponent.tsx
|  `- OneComponent.tsx
|- middleware.ts
`- reducer.ts
```

- All new features must be written in TypeScript.
- When working on older features, converting JavaScript to TypeScript is encouraged.
- Import middleware in `react/features/app/` in `middlewares.any`, `middlewares.native.js`, or `middlewares.web.js` as appropriate.
- Import reducers in the appropriate app wiring location as well.

### Index File Guidance

In general, avoid index files and prefer full import paths.

Exception: when common code must import platform-specific components, create:

- `components/index.native.ts`
- `components/index.web.ts`

Export only what is needed, and import common code from `components/index`.

Older code may not follow this pattern, but new features should. Migrating older features is encouraged when practical.

### Avoiding Bundle Bloat

If a new feature causes a bundle-size-related build failure, analyze first before increasing limits.

1. Build with analysis enabled:

```bash
npx webpack -p --analyze-bundle
```

2. Open the analyzer:

```bash
npx webpack-bundle-analyzer build/app-stats.json
```

## Kotlin

For Kotlin code, use standard Kotlin conventions and keep line length at 120 characters. Formatting is enforced with `ktlint`.

## Code Reviews

1. Submit your contribution.
2. Consider opening a draft PR early for design and implementation discussion.
3. Appropriate reviewers are assigned based on affected code areas.
4. Reviewers evaluate standards, correctness, performance, and risk.
5. Address feedback and iterate.
6. Once the PR is in good shape, a team member triggers automated tests.
7. The PR must merge cleanly on top of `master`, and failing checks must be fixed before approval.
8. After review and test success, the PR is approved for merge.

## Issue Closing

You can close issues automatically using GitHub closing keywords in pull requests and commit messages.
