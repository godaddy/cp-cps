## Linting

All VMC certificates are linted prior to signing. If a lint fails, issuance is aborted
and engineering triages the cause, which may relate to request data, certificate profile
configuration, issuance system configuration, or lint rule interpretation. Corrections
and tests are applied as required, and issuance resumes only after successful re-linting.

### Post-Issuance Monitoring
GoDaddy performs scheduled post-issuance linting across active VMC certificate inventory
to detect issues and validate the effectiveness of issuance controls. In addition, we
audit and lint at least 3% of all certificates issued by the CA on an ongoing basis.

### Tooling and Update Management
GoDaddy uses ZLint, CertLint, PKIMetal, and an internally developed linter. Engineering
monitors upstream changes to these tools and their rulesets, evaluates new or modified
lints, and deploys updates to production following internal testing and validation.

### Skip Lints
Subscriber certificates are validated without skipping any lints. For CA root and
intermediate testing, narrowly scoped, temporary lints may be skipped only when a rule
is not applicable, with documented justification and review.

### Continuous Improvement and Contributions
GoDaddy actively contributes to open-source linting tooling used across the Web PKI
ecosystem. We recently contributed a fix to PKIMetal correcting the zlint handling for
Authority Revocation Lists (ARLs) under the tbr_arl profile. Previously, ARLs were
incorrectly evaluated using the subscriber CRL 10-day nextUpdate limit rather than the
correct 12-month CA/ARL limit defined in the TLS Baseline Requirements. Our fix added
a separate zlint registry for TLS BR ARLs to ensure correct validation behaviour. This
contribution was merged into PKIMetal and included in v1.48.0.

We have also previously contributed to CertLint after identifying a gap in coverage
around linting CA intermediate certificates. We will continue to contribute fixes and
improvements to ecosystem linting tooling when further opportunities are discovered.
