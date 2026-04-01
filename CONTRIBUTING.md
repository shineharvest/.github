# Contributing to Shine Harvest

## Program Context

Shine Harvest is a controlled space-based solar power engineering program. This is not an open-source project. All contributions require team membership and appropriate permissions within the `shineharvest` GitHub organization.

## Contribution Process

1. **Check your permissions.** Ensure you are a member of the appropriate team for the repository you are contributing to. See the Program Handbook for the team-repo permission matrix.

2. **Follow repo-specific guidance.** Each repository has its own `CONTRIBUTING.md` with scope-specific rules. Read it before opening a pull request.

3. **Branch from `develop`.** All work branches must be created from the `develop` branch. Direct commits to `main` are prohibited.

4. **Use pull requests.** All changes go through pull requests. CODEOWNERS review is mandatory. The required number of approvals depends on the repository criticality level.

5. **Squash merge only.** All repositories are configured for squash merges. This produces a clean, linear commit history on `main` and `develop`.

6. **No force-push.** Force-pushing to `main` or `develop` is prohibited under all circumstances.

## Engineering Standards

- **State terms** must come from the program state dictionary (`sh-architecture/docs/state-dictionary-v0.1.md`). Do not invent local state vocabulary.
- **Requirements** must use the `SH-XXX-NNN` format (e.g., `SH-SYS-001`, `SH-BMC-003`).
- **Interface changes** must reference an ICD number and be reflected in the cross-repo interface dependency matrix.
- **Baselined documents** require a change record before modification.
- **Verification cases** must use the `XRV-NNN` or `XRV-SOL-NNN` format.

## Documentation Requirement

Every substantive code or model change must have a corresponding documentation update. Undocumented state changes, interface modifications, or baseline revisions are not acceptable.

## What Not To Do

- Do not create new repositories without program-level approval
- Do not commit credentials, API keys, or operationally sensitive data (GPS coordinates, site locations)
- Do not modify signed review records in `sh-verification`
- Do not bypass CODEOWNERS review
- Do not treat simulation results as verified evidence without VNV review

## Questions

Direct program-level questions to the `systems-architecture` team via GitHub Discussions in `sh-architecture`.
