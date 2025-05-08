# hmpo-node-standards

This `hmpo-node-standards` is a shared dependency that helps standardise code across HMPO services.

## Installation

Add `hmpo-node-standards` to your project’s `package.json`. For example.

```json
  "devDependencies": {
    "hmpo-node-standards": "^2.0.0"
  }
```

## Usage

`checkengines` verifies if the current Node and npm version match the required version in `package.json`, if `engineStrict` is set to true.

`checkgit` prevents force pushes, deletions and uncommitted changes of protected branches.

`comparelocales` checks for missing translation keys between two locales (English and Welsh). Fails if any keys are missing.

`commitmsg` enforces proper commit message formatting by ensuring that each commit starts with either a JIRA ticket ID or an approved prefix. Valid commit prefixes include:

- ABC-1234 Commit message.

- CHORE: Commit message.

- NOJIRA: Commit message.

- WIP: Commit message.

`lintapostrophes` verifies correct apostrophe usage in files.

`semver` can be used to compare two semantic versions of your Node.js app. It checks whether the first version satisfies the constraint that is defined by the second version. For example:

- Version 1.2.3 compared to ^1.2.0 passes, because ^1.2.0 allows any version from 1.2.0 up to (but not including) 2.0.0.
- Version 1.2.3 compared to ^2.0.0 fails, because 1.2.3 is less than 2.0.0 which does not satisfy the constraint.

`update-package` add hmpo standard scripts to your `package.json` if dependencies are present.