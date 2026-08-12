## GoDaddy CA Values & Benefits Statement

### Overview and Value to Apple
GoDaddy operates a resilient, distributed public key infrastructure designed for high
availability, reliable certificate lifecycle management, and standards-compliant issuance
and revocation. Through our SSL API and certificate management platform, we support
secure, scalable certificate deployment for a broad range of subscribers, helping expand
the availability of trusted digital identity across diverse platforms, applications, and
geographies.

For Apple, this provides value through the continued availability of a mature CA service
with established operational controls, broad customer reach, and ongoing investment in
reliability engineering, automation, monitoring, and compliance. These capabilities support
Apple's goals of maintaining a secure and interoperable ecosystem for users and developers.

The new GoDaddy roots requested for inclusion are intended to support the issuance of
Verified Mark Certificates (VMC), enabling organizations to display authenticated brand
logos in supported email clients. This request reflects GoDaddy's expansion into the VMC
space and aligns with our commitment to supporting modern digital identity and trust use
cases for Apple users and the broader ecosystem.

### Security, Compliance, and Transparent Incident Reporting
GoDaddy maintains a security and compliance program designed to protect CA systems,
subscriber information, and certificate issuance processes. This program includes continuous
monitoring, vulnerability management, secure software development practices, infrastructure
and application security reviews, and periodic control assessments performed by dedicated
security teams.

GoDaddy maintains documented incident response and escalation procedures that support
timely detection, triage, containment, remediation, and stakeholder notification. When
compliance or operational incidents occur, we perform root-cause analysis, implement
corrective and preventive actions, and provide transparent public disclosure through standard
industry channels, including CCADB when applicable. These processes are intended to ensure
timely and transparent reporting and to support continued trust in our CA operations.

### Audit, Policy Maintenance, and Alignment with Industry Standards
GoDaddy's CA operations are governed by controlled policies and procedures designed to
align with the CA/Browser Forum Requirements, root store program requirements, and
applicable audit criteria. Our Certificate Policy and Certification Practice Statement
(CP/CPS) are maintained through a structured governance process that includes version
control, internal stakeholder review, legal review, and formal review at least annually,
with updates made as needed to reflect evolving requirements.

GoDaddy undergoes annual independent WebTrust audits for its publicly trusted CA
operations and maintains CA disclosure information in CCADB in accordance with ecosystem
expectations. These processes reflect our commitment to policy accuracy, audit readiness,
and continuous conformance with applicable PKI standards.

### Privacy and Protection of User Information
GoDaddy collects and processes information necessary to validate certificate requests and
operate CA services at the appropriate assurance level. Such processing is limited to
legitimate CA purposes, including validation, issuance, revocation, compliance, security
monitoring, and record retention as required by applicable policies and program rules.

GoDaddy aligns its privacy practices with the Starfield Technologies Privacy Policy,
including principles of transparency, data minimization, appropriate retention, and
protection of user information. GoDaddy does not sell certificate applicant information
and limits sharing of data to circumstances necessary for CA operations, service delivery,
legal obligations, or compliance with applicable standards and root program requirements.

### Participation in the CA Community
GoDaddy participates in the CA/Browser Forum and other relevant industry discussions and
contributes through working groups, technical feedback, and practical implementation
experience. We support the continued development of baseline requirements, incident
handling practices, and improvements to certificate profiles, validation methods, and
operational expectations across the public trust ecosystem.

When opportunities arise to improve ecosystem conformance, GoDaddy contributes to
tooling and implementation practices that strengthen interoperability and standards
adherence. We have implemented a static Certificate Transparency log, including for
VMC certificate transparency. We also actively contribute to open-source linting
tooling used across the ecosystem. Most recently, we contributed a fix to PKIMetal
addressing incorrect zlint handling for Authority Revocation Lists (ARLs), which were
previously subject to the wrong nextUpdate limit. This fix was merged into PKIMetal
and included in v1.48.0.

When opportunities arise to improve ecosystem conformance, GoDaddy contributes to tooling and implementation practices that strengthen interoperability and standards adherence. We have implemented a static Certificate Transparency log for VMC certificate transparency. Most recently, GoDaddy contributed to the Sunlight static CT implementation, enabling Sunlight to operate CT logs specifically configured to accept and validate Mark Certificates, including validation of the required Verified Mark Certificate EKU.

### Future Goals and Alignment with the CA Ecosystem
GoDaddy's future goals as a CA are aligned with the broader goals of the public trust
community: strong security controls, reliable validation, resilient operations, transparent
incident handling, support for modern cryptographic and certificate profile requirements,
and responsible lifecycle management of roots and subordinate hierarchies.

A key initiative in this effort is the expansion of our CA capabilities to support Verified
Mark Certificates, reflecting our commitment to supporting evolving digital identity use
cases and modern trust requirements. This is complemented by our ongoing work on root
lifecycle management, single-use root hierarchies, and the adoption of updated technical
and compliance requirements as they evolve.

### Commitment to Apple Users and Developers
GoDaddy is committed to maintaining secure, reliable, and transparent CA operations that
support the safety of Apple users and the needs of Apple developers. We continuously
improve our automation, monitoring, policy governance, and operational controls; adopt
evolving industry standards; communicate transparently with root programs; and responsibly
phase out legacy practices in accordance with industry consensus.

Through these efforts, GoDaddy seeks to provide ongoing value to Apple by supporting a
more secure, privacy-conscious, interoperable, and resilient digital identity ecosystem,
including through the trusted issuance of Verified Mark Certificates for use by Apple users
and developers.

### Certificate Transparency Support for VMC
GoDaddy supports Certificate Transparency for VMC certificates. We have recently
announced the implementation of a dedicated static CT log for VMC certificate
transparency. Details of this announcement are publicly available at the following [link](https://groups.google.com/g/certificate-transparency/c/AVqBtti9pZA/m/jTXLfjGiBwAJ).

GoDaddy intends for this VMC-specific CT log to be accepted by the AuthIndicators Working Group as an alternative to the Gorgon CT Log.

This CT log has been implemented to enhance transparency and accountability in VMC
certificate issuance and to align with the evolving expectations of publicly trusted PKI
environments. Through this initiative, GoDaddy contributes to the resilience and diversity
of the CT ecosystem for VMC certificates and supports Apple's expectations for transparent
and accountable certificate operations.
