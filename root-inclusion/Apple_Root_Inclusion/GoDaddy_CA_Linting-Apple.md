## Linting Summary

All certificates are linted prior to signing. If a lint fails, issuance is aborted and engineering triages the cause (data, profile, or configuration). Corrections and tests are applied as required, and issuance resumes only after successful re‑linting.

### Post‑issuance Monitoring
GoDaddy performs scheduled post-issuance linting across active certificate inventory and CT-sourced samples to detect issues and validate the effectiveness of issuance controls. In addition, we audit and lint at least 3% of all certificates issued by the CA on an ongoing basis.

### Tooling and update management
GoDaddy uses ZLint, CertLint, and an internally developed linter. Engineering monitors upstream changes to these tools and their rulesets, evaluates new or modified lints, and deploys updates to production following internal testing and validation.

### Skip Lints
Subscriber certificates are validated without skipping any lints. For CA root and intermediate testing, narrowly scoped, temporary lints may be skipped only when a rule is not applicable, with documented justification and review.

### Continuous improvement and contributions 
We recently contributed to CertLint after identifying a gap in coverage around linting CA intermediate certificates. We will continue to contribute fixes and improvements when further opportunities are discovered. 
