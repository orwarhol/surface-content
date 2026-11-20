# Security reporting

Surface Content is a text-only agent skill. Unsafe instructions, unintended expansion of editorial permissions, compromised release provenance or accidental disclosure are meaningful security concerns even without executable code.

Use the repository's [Security advisories](https://github.com/orwarhol/surface-content/security/advisories) private reporting option when available. Verify that the form is private before submitting. If private reporting is not yet enabled, do not include sensitive information in a public issue; request a private contact using a nonsensitive issue with no vulnerability details.

Include the affected release or commit, the agent and mode, the expected boundary, the observed behavior, and the smallest synthetic reproduction. Never include credentials, private customer content, access tokens or a live target. For a nonsensitive documentation bug, use ordinary issues.

The package is currently a pre-release candidate. The maintainer must confirm that private vulnerability reporting and notifications are enabled and monitored before promoting the first release. No response-time guarantee is made. A confirmed unsafe revision should be identified in release notes or an advisory and corrected in a new reviewed release. Review and deliberately replace affected installed copies; they cannot be recalled remotely.
