## GoDaddy Value Statement for Mozilla Root Inclusion

### Executive Summary
We are requesting inclusion of new publicly trusted TLS roots intended to replace existing GoDaddy and Starfield roots currently used for publicly trusted TLS issuance. These successor roots are part of our transition to single-use PKI root hierarchies and a more regular root lifecycle model.

The purpose of this request is not to expand into new trust purposes, but to support continued service for existing subscriber populations through updated hierarchies designed for improved maintainability, clearer scoping, and more agile lifecycle management. Inclusion of these roots would support Mozilla users by enabling an orderly migration away from older root hierarchies while maintaining continuity for certificates and services relied upon by Firefox users.

This statement is organized around Mozilla’s three value themes: user value and impact, compliance maturity and risk management, and transparency and public accountability.

### 1. User Value and Impact
Our publicly trusted TLS services support subscribers whose websites and online services are directly accessed by Mozilla users. The roots covered by this request are intended to replace currently active roots serving existing subscriber populations, rather than introduce new trust purposes.

GoDaddy operates at scale, issuing and managing more than 160 million TLS certificates across a wide range of customers — from small businesses to large enterprises — with robust automation, monitoring, and revocation capabilities. We also support multiple geographic markets and provide support in multiple languages. 

These certificates secure services directly relied upon by Firefox users for encrypted web connections.

We support certificate lifecycle management through automation interfaces such as ACME and API-based workflows. A majority of our TLS subscriber certificates use automation, and approximately 95% of issued TLS subscriber certificates are expected to use automation. We make ACME available to all prospective subscribers, require external account binding, and support ACME Renewal Information. We also perform multi-perspective domain validation for TLS subscriber certificates. 

These capabilities improve user security and reliability by reducing manual handling risk, supporting more consistent validation outcomes, improving certificate deployment and renewal at scale, and reducing the likelihood of avoidable issuance and operational errors. Automation also helps reduce the risk of certificate expiration-related outages, which can otherwise interrupt access to secure services relied upon by Mozilla users. 

We also maintain high availability for revocation infrastructure, including OCSP and CRL services, to support timely and reliable certificate status checking, with 100% uptime for 2025 and 2026 year to date. This helps relying parties continue to make informed trust decisions and improves the resilience of the overall certificate ecosystem.

GoDaddy aligns with Mozilla’s mission to make the internet open, accessible, and secure by supporting most geographic regions and through internal initiatives such as the upcoming operation of a GoDaddy-managed CT log. This will further enhance transparency and reduce ecosystem dependency on a small number of log operators, directly benefiting Mozilla users by improving log redundancy, performance and security. 

Our impact is demonstrated by issuing 160 million TLS subscriber certificates, with about 95% automated.

Our inclusion also provides a return on Mozilla’s investment in oversight by supporting an existing subscriber population through mature, audited CA operations with broad automation, structured lifecycle planning, and controls designed to reduce operational risk and improve predictability over time.

### 2. Compliance Maturity and Risk Management

#### 2.1 Commitment and Resourcing
GoDaddy has made a long-term commitment to operating publicly trusted CA services and have invested in infrastructure, personnel, audit functions, and governance processes to support those operations.

One hundred percent of personnel operating our CA are full-time employees. We maintain multiple teams with varying roles from engineering to GRC Compliance that are dedicated to Risk and Compliance. Six GoDaddy employees are participants of various CAB Forum working groups. We have also invested in technical compliance expertise, including a Technical Compliance Manager, Rob White. Rob previously served as a Manager at BDO, where he worked in their PKI Compliance department. In this role, he managed WebTrust, SOC 2, and ISO engagements for CA/Browser Forum members, including Microsoft PRSS, Amazon Trust Services, DigiCert, Sectigo, IdenTrust, and Let’s Encrypt. He also performed internal control gap assessments and supported WebTrust long-form reporting for Certificate Authorities.

Our compliance resourcing is determined through ongoing operational planning that takes into account the scope of our publicly trusted CA activities, applicable root program and CA/Browser Forum requirements, audit obligations, incident response readiness, and planned infrastructure or product changes. Compliance-related investment is not treated as a fixed point-in-time budget item; it is evaluated as part of the broader staffing, engineering, security, and operational support required to maintain compliant CA operations. 

Recent and ongoing investments include modernization of our CA infrastructure, implementation and rollout of the R1 hierarchy, rollout of Mark Certificate offerings, and continued development of Certificate Transparency capabilities, including development of CT log hosting infrastructure. 

This approach is intended to ensure that compliance capacity remains aligned with operational complexity and ecosystem expectations, rather than remaining static as requirements evolve. 

#### 2.2 Personnel and Expertise
Our dedicated compliance staff including our new Technical Risk Manager are responsible for tracking updates to CA/Browser Forum Requirements, Community Bugzilla Incidents, Root Store Program Requirements, RFCs, audit criteria, and related PKI Standards as part of ongoing CA operations. Changes to compliance requirements are documented in Jira, and tasks are automatically created for internal PKI stakeholders to evaluate impacts across engineering, technical risk, and product management. These changes are then presented and discussed in a weekly PKI Compliance sync to ensure action items are assigned and completed. In addition, upon hire and on an annual basis, GoDaddy Trusted Roles are required to complete PKI Trusted Role training that covers CP/CPS requirements, CA/Browser Forum and root program requirements, certificate validation and issuance controls, audit and evidence-handling expectations, incident reporting and revocation obligations, change management, and lessons learned from internal and industry compliance incidents.

GoDaddy actively participates in CA/Browser Forum working groups. In the past two years, we have attended close to 99% of CA/B Forum Face-to-Face meetings, NetSec Working Group meetings, Server Certificate Working Group meetings, Validation Subcommittee meetings, and voting on CAB Ballots.

We regularly review incidents reported in Bugzilla and other public Web PKI forums to identify patterns, control gaps, and lessons relevant to our own CA operations. This includes both incidents involving our own organization and publicly discussed incidents across the ecosystem, with particular focus on validation failures, revocation timing issues, certificate profile errors, and operational or process breakdowns. 

We integrate lessons learned from these incidents into our operations through updates to validation logic, linting, automated testing, certificate profiles, internal procedures, compliance tracking workflows, and change management processes. Incident learnings are also used to improve escalation paths, remediation planning, and policy-to-system alignment across engineering, compliance, and operational teams. 

Our general view is that many recurring Web PKI incidents arise from CP/CPS requirements not being fully reflected in implementation or from avoidable system misconfigurations. As a result, we emphasize automation, programmatic enforcement, and continuous testing as key mechanisms for reducing the likelihood of similar issues in our own environment.

#### 2.3 Operational Design for Compliance
Our CA systems and workflows are designed to support compliance with the CA/Browser Forum Baseline Requirements, Mozilla Root Store Policy, and applicable audit criteria.

We use an event-driven architecture that programmatically enforces required validations throughout the lifecycle of subscriber certificate requests. We also operate staging and test infrastructure to evaluate updates and feature enhancements prior to production deployment.

Controls include:
•	pre-issuance certificate linting,
•	documented certificate profiles and issuance logic,
•	multi-perspective domain validation,
•	validation controls appropriate to certificate type,
•	controlled policy and CPS governance,
•	change management processes, and
•	incident escalation and remediation procedures.
All publicly trusted subscriber certificates are linted prior to signing using ZLint, CertLint, and internally developed linting checks. If a lint fails, issuance is aborted, the issue is triaged, and issuance resumes only after correction, testing, and successful re-linting.

We also perform scheduled post-issuance linting across active certificate inventory and CT-sourced samples and audit and lint at least 3% of all certificates issued by the CA on an ongoing basis.

Processes are documented and enforced through controlled operational procedures, system workflows, configuration management, and review practices. We maintain agility through ongoing monitoring of evolving standards and deploy updates to tools, rules, configurations, and issuance workflows following internal review and testing.

All CA-related teams are assigned goals and KPI targets to maintain full compliance with CA requirements and to ensure that identified compliance incidents are effectively remediated through comprehensive improvements.

#### 2.4 Compliance Program and Third-Party Oversight
Our publicly trusted CA operations are supported by a compliance framework aligned to applicable WebTrust criteria, CA/Browser Forum requirements, root program requirements, and broader organizational security and risk management practices. GoDaddy has been operational since 2004.

We plan to maintain continuous WebTrust audits for these hierarchies, and all CA certificates corresponding to the hierarchies are within a single audit scope. Our policy documents are maintained in a combined CP/CPS, are free-standing, and are available in Markdown format.

GoDaddy’s WebTrust audits are performed by CPA Canada enrolled WebTrust practitioner Schellman and Company, LLC. The Schellman team have extensive experience in auditing information technology environments, including commercial PKI and WebTrust examinations, with the range of 12 to 30 years of PKI experience. The team also posses a number of technical certifications including CISSP, CISA, CEH and CPA. 

GoDaddy undergo annual independent WebTrust audits for our publicly trusted CA operations and maintain CA disclosure information in CCADB in accordance with ecosystem expectations. Our Certificate Policy and Certification Practice Statement documents are maintained through structured governance processes including version control, internal review, legal review, and formal review at least annually.

Identified deficiencies are documented, tracked, remediated, and reviewed through established corrective action processes. Management oversight supports accountability for compliance, audit readiness, policy maintenance, and risk reduction.

### 3. Transparency and Public Accountability
We recognize that public trust in the Web PKI depends on transparency, timely disclosure, and constructive engagement with root programs and the broader compliance community.

In the last two years, we have had more than one self-reported CA incident disclosed to Bugzilla. Our incident history does not reflect a sustained pattern of repeated incidents of a similar nature. Incident handling is performed within our compliance program and is continually being executed and improved.  

We participate in public compliance processes within CCADB, public incident discussion and follow-up, and public discussion groups. When compliance or operational incidents occur, we maintain documented incident response and escalation procedures that support detection, triage, remediation, root-cause analysis, corrective action, and public disclosure through standard industry channels.

We communicate and cooperate with root programs during incident handling and other significant compliance matters. Our processes are intended to support timely reporting, clear follow-up, and sustained remediation.

We also contribute to broader ecosystem accountability through participation in the CA/Browser Forum and related industry discussions. We support the development of baseline requirements, incident handling practices, certificate profile improvements, validation updates, and other ecosystem standards. Where opportunities arise, we contribute to tooling and implementation practices that improve interoperability and conformance. We recently contributed to CertLint after identifying a gap in coverage around linting CA intermediate certificates.

GoDaddy also actively participates in community initiatives such as ACME, CT logging. The planned operation of a GoDaddy-managed CT log will further enhance transparency and reduce ecosystem dependency on a small number of log operators, directly benefiting Mozilla users by improving log redundancy, performance, and auditability.

Publicly available materials supporting accountability include CP/CPS documentation, audit reports, privacy policy materials, help center resources, CCADB disclosures, and crt.sh entries for the relevant roots and cross-signatures.

### 4. Root Lifecycle and Customer Transition Context
The roots requested for inclusion are successor roots intended to replace currently active GoDaddy and Starfield G2 roots used for publicly trusted TLS issuance.

#### Active Roots in Operation

| Root Common Name | crt.sh | Not After | Key Algorithm | Key Size | Signing Algorithm |
| --- | --- | --- | --- | --- | --- |
| Go Daddy Root Certificate Authority - G2 | [crt.sh 548406](https://crt.sh/?id=548406) | 2037-12-31 | RSA | 2048 | SHA-256 |
| Starfield Root Certificate Authority - G2 | [crt.sh 221795](https://crt.sh/?id=221795) | 2037-12-31 | RSA | 2048 | SHA-256 |

#### Successor Roots

| Root Common Name | crt.sh | Not After | Key Algorithm | Key Size | Signing Algorithm | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| GoDaddy TLS Root CA - R1 | [crt.sh 20878431179](https://crt.sh/?id=20878431179) | 2040-08-24 | RSA | 4096 | SHA-256 | Successor signed ahead of G2 expiry; inclusion requested. |
| Starfield TLS Root CA - R1 | [crt.sh 20878454206](https://crt.sh/?id=20878454206) | 2040-08-23 | RSA | 4096 | SHA-256 | Successor signed ahead of G2 expiry; inclusion requested. |

These successor roots were generated in advance of G2 expiration as part of our long-term lifecycle management approach. We plan to create new subordinate CAs annually and aim to migrate issuance from one generation of root CAs to the next every five years beginning with these new root CA certificates.

Our root lifecycle strategy includes a long-term goal of more regular root replacement, limited and temporary use of cross-signatures to support migration, and retirement of deprecated hierarchies once subscriber transitions are complete. We do not plan to issue cross-certificates that extend the Mozilla trust boundary.

The G2 to R1 transition is actively already begun and will conclude no later than September 2026. We support subscriber transition through public support resources, targeted subscriber communications, in-product notifications where applicable, partner communications, and account-based contact management processes.

### 5. Conclusion
We believe inclusion of these successor roots would provide value to Mozilla users by supporting continuity for an existing population of TLS subscribers while enabling transition to more maintainable, clearly scoped, and modern root hierarchies. 

Our publicly trusted CA operations are supported by structured compliance controls, annual independent audits, certificate quality mechanisms such as pre-issuance linting, and incident handling processes designed to support accountability and continuous improvement. Our operations also reflect dedicated staffing, broad automation of issuance, active standards participation, and ongoing investment in modernizing our PKI.

