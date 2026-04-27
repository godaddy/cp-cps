## GoDaddy CA Value Statement for Microsoft Root Inclusion

### Overview and Value to Microsoft
GoDaddy operates a resilient, distributed public key infrastructure designed for high availability, reliable certificate lifecycle management, and standards-compliant issuance and revocation. Through automation interfaces such as ACME and our SSL API, we support secure, scalable certificate deployment for a broad range of subscribers, helping expand the availability of trusted TLS across diverse platforms, applications, and geographies.

For Microsoft, this provides value through the continued availability of a mature CA service with established operational controls, broad customer reach, and ongoing investment in reliability engineering, automation, monitoring, and compliance. These capabilities support Microsoft’s goals of maintaining a secure, interoperable, and resilient ecosystem for users, developers, and relying parties.

The new GoDaddy roots requested for inclusion are intended to replace existing roots currently relied upon in public trust programs. This transition supports GoDaddy’s move toward single-use PKI root hierarchies, which improves transparency, simplifies root management, and aligns with current industry best practices for long-term PKI agility and risk reduction.

### Security, Compliance, and Transparent Incident Reporting
GoDaddy maintains a security and compliance program designed to protect CA systems, subscriber information, and certificate issuance processes. This program includes continuous monitoring, vulnerability management, secure software development practices, infrastructure and application security reviews, and periodic control assessments performed by dedicated security teams.

GoDaddy maintains documented incident response and escalation procedures that support timely detection, triage, containment, remediation, and stakeholder notification. When compliance or operational incidents occur, we perform root-cause analysis, implement corrective and preventive actions, and provide transparent public disclosure through standard industry channels, including CCADB when applicable. These processes are intended to ensure timely and transparent reporting and to support continued trust in our CA operations.

### Audit, Policy Maintenance, and Alignment with Industry Standards
GoDaddy’s CA operations are governed by controlled policies and procedures designed to align with the CA/Browser Forum Requirements, root store program requirements, and applicable audit criteria. Our Certificate Policy and Certification Practice Statement (CP/CPS) are maintained through a structured governance process that includes version control, internal stakeholder review, legal review, and formal review at least annually, with updates made as needed to reflect evolving requirements.

GoDaddy undergoes annual independent WebTrust audits for its publicly trusted CA operations and maintains CA disclosure information in CCADB in accordance with ecosystem expectations. These processes reflect our commitment to policy accuracy, audit readiness, and continuous conformance with applicable PKI standards.

### Privacy and Protection of User Information
GoDaddy collects and processes information necessary to validate certificate requests and operate CA services at the appropriate assurance level. Such processing is limited to legitimate CA purposes, including validation, issuance, revocation, compliance, security monitoring, and record retention as required by applicable policies and program rules.

GoDaddy aligns its privacy practices with the Starfield Technologies Privacy Policy, including principles of transparency, data minimization, appropriate retention, and protection of user information. GoDaddy does not sell certificate applicant information and limits sharing of data to circumstances necessary for CA operations, service delivery, legal obligations, or compliance with applicable standards and root program requirements.

### CA Lifecycle Management
GoDaddy’s CA lifecycle management strategy is designed to support regular root replacement, modern key management practices, controlled migration planning, and timely retirement of legacy hierarchies. Our current transition from the G2 root generation to the R1 root generation reflects our move toward single-use root hierarchies and a long-term operating model that supports more regular root rotation, improved cryptographic hygiene, and simplified trust management.

#### Active Roots in Operation
The following roots are currently in active operation for publicly trusted TLS issuance:

| Root Common Name | crt.sh | Not After | Key Algorithm | Key Size | Signing Algorithm |
| --- | --- | --- | --- | --- | --- |
| Go Daddy Root Certificate Authority - G2 | [crt.sh 548406](https://crt.sh/?id=548406) | 2037-12-31 | RSA | 2048 | SHA-256 |
| Starfield Root Certificate Authority - G2 | [crt.sh 221795](https://crt.sh/?id=221795) | 2037-12-31 | RSA | 2048 | SHA-256 |

#### Successor Roots
The following successor roots have been generated to replace the currently active G2 roots:

| Root Common Name | crt.sh | Not After | Key Algorithm | Key Size | Signing Algorithm | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| GoDaddy TLS Root CA - R1 | [crt.sh 20878431179](https://crt.sh/?id=20878431179) | 2040-08-24 | RSA | 4096 | SHA-256 | Successor signed ahead of G2 expiry; inclusion requested. |
| Starfield TLS Root CA - R1 | [crt.sh 20878454206](https://crt.sh/?id=20878454206) | 2040-08-23 | RSA | 4096 | SHA-256 | Successor signed ahead of G2 expiry; inclusion requested. |

#### Replacement Signing Cadence
New GoDaddy roots have a 15-year validity period with a long-term goal of targeting successor root signing every four years to enable a future five-year root rotation model for the WebPKI.

#### Cross-Signatures Between Generations
GoDaddy’s G2 roots have cross-signed the new R1 successors to ensure path continuity during migration. Cross-signatures are limited in scope and duration to reduce chain complexity while enabling smooth subscriber transitions.

All R1 roots and their intermediate certificates are signed with the SHA-256 signature algorithm.

| Common Name | crt.sh | Not After | Key Algorithm | Key Size | Signing Algorithm | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| GoDaddy TLS Root CA - R1 | [crt.sh 21408225576](https://crt.sh/?id=21408225576) | 2040-08-24 | RSA | 4096 | SHA-256 | Cross-signed by Go Daddy Root Certificate Authority - G2 |
| Starfield TLS Root CA - R1 | [crt.sh 21408224860](https://crt.sh/?id=21408224860) | 2040-08-23 | RSA | 4096 | SHA-256 | Cross-signed by Starfield Root Certificate Authority - G2 |

#### Trust Purposes
Both GoDaddy G2 and Starfield G2 are scoped for TLS server authentication, including DV, OV, and EV issuance where applicable. The separate chains serve distinct customer segments and have been in continuous operation since 2009.

#### Cryptographic Profiles
Active G2 roots use RSA 2048. Successor R1 roots use RSA 4096. All R1 root and intermediate certificates use the SHA-256 signing algorithm. Subscriber certificates are issued with RSA 2048 or RSA 4096 keys. GoDaddy will continue to adopt approved profiles and algorithms as appropriate.

#### Customer Transition Timeline
The G2 to R1 transition is planned for approximately four months, subject to platform inclusion timing and customer deployment readiness. This rotation removes the ClientAuth EKU from subscriber certificates, and we are operationalizing transitions to accelerate future rotations.

#### Root Store Submission and Retirement Planning
New roots are submitted to root programs at the earliest practical opportunity after Root Generation Audit reports and related artifacts are finalized, allowing sufficient review and distribution lead time.

Deprecated roots can be removed after subscriber transitions are complete. GoDaddy will coordinate retirement timing with applicable root programs to minimize ecosystem impact and ensure timely removal once legacy hierarchies are no longer required.

### Customer and Change Management
GoDaddy maintains customer and change management processes intended to support orderly subscriber transitions, timely communication of operational changes, and effective coordination with customers and partners during certificate lifecycle events.

GoDaddy provides publicly accessible help articles and related support resources that announce upcoming certificate and platform changes, describe implementation timelines, and explain expected customer impacts. These resources are reviewed and updated as plans evolve so that subscribers, partners, and relying parties have current guidance.

GoDaddy communicates upcoming changes to existing subscribers through multiple channels, including targeted email to account contacts, public help articles, in-product notifications where applicable, and partner communications. These communications are intended to clearly describe timelines, required customer actions, and any expected subscriber-specific impacts.

GoDaddy maintains subscriber contact information through customer account profiles and related account management processes. Customers are able to update their contact details as needed, and these records are used to support customer notifications relating to certificate lifecycle events and operational changes.

GoDaddy gathers input from customers through support interactions, direct communications, and regular engagement with industry partners and integrators. This feedback is considered as part of implementation planning, customer communication strategy, and transition timing where appropriate.

### Linting and Certificate Quality Controls
All publicly trusted subscriber certificates are linted prior to signing. GoDaddy uses ZLint, CertLint, and an internally developed linter as part of the issuance workflow. If a lint fails, issuance is aborted and engineering triages the cause, including data, profile, configuration, or rule interpretation. Corrections and testing are performed as needed, and issuance resumes only after successful re-linting.

GoDaddy performs scheduled post-issuance linting across active certificate inventory and CT-sourced samples to detect issues and validate the effectiveness of issuance controls. In addition, we audit and lint at least 3% of all certificates issued by the CA on an ongoing basis.

Engineering monitors upstream changes to linting tools and rulesets, evaluates new or modified lints, and deploys updates to production following internal testing and validation.

Subscriber certificates are validated without skipping any lints. For CA root and intermediate testing, narrowly scoped, temporary lint suppressions may be used only when a rule is not applicable, with documented justification and review.

GoDaddy reviews new and updated lints as part of ongoing maintenance of its linting controls. We recently contributed to CertLint after identifying a gap in coverage around linting CA intermediate certificates and will continue to contribute fixes and improvements when further opportunities are discovered.

### Participation in the CA Community
GoDaddy participates in the CA/Browser Forum and other relevant industry discussions and contributes through working groups, technical feedback, and practical implementation experience. We support the continued development of baseline requirements, incident handling practices, and improvements to certificate profiles, validation methods, and operational expectations across the public trust ecosystem.

In addition, when opportunities arise to improve ecosystem conformance, GoDaddy contributes to tooling and implementation practices that strengthen interoperability and standards adherence. We are also pursuing the implementation of a static Certificate Transparency log, with the goal of qualifying as a trusted CT log operator and contributing to the resilience and diversity of the CT ecosystem.

### Future Goals and Alignment with the CA Ecosystem
GoDaddy’s future goals as a CA are aligned with the broader goals of the public trust community: strong security controls, reliable validation, resilient operations, transparent incident handling, support for modern cryptographic and certificate profile requirements, and responsible lifecycle management of roots and subordinate hierarchies.

A key initiative in this effort is the operationalization of new root generation to support regular five-year root rotation and a single-use root strategy. This approach is intended to improve long-term maintainability, reduce complexity, and enable more agile adoption of updated technical and compliance requirements.

### Commitment to Microsoft Users and the Web PKI Ecosystem
GoDaddy is committed to maintaining secure, reliable, and transparent CA operations that support the safety of Microsoft users, the needs of developers, and the health of the broader Web PKI ecosystem. We continuously improve our automation, monitoring, policy governance, and operational controls; adopt evolving industry standards; communicate transparently with root programs; and responsibly phase out legacy practices in accordance with industry consensus.

Through these efforts, GoDaddy seeks to provide ongoing value to Microsoft by supporting a more secure, privacy-conscious, interoperable, and resilient TLS ecosystem.
