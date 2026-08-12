## GoDaddy CA Lifecycle Management

### Overview
GoDaddy's CA lifecycle management strategy is designed to support regular root replacement,
modern key management practices, controlled migration planning, and timely retirement of
legacy hierarchies. The GoDaddy Verified Mark Root CA - VMCR1 represents a brand new
hierarchy established to support the issuance of Mark Certificates, with
no predecessor root.

### Active Roots in Operation
The following root is currently in operation for VMC issuance:

| Root Common Name | Not After | Key Algorithm | Key Size | Signing Algorithm |
| --- | --- | --- | --- | --- |
| GoDaddy Verified Mark Root CA - VMCR1 | 2040-08-24 | RSA | 4096 | SHA-256 |

### Planned Roots
GoDaddy currently plans for one VMC root corresponding to the hierarchy described in
this request. As this is a new hierarchy with no predecessor root, there are no successor
roots planned at this time. Future root replacement will follow GoDaddy's standard
lifecycle management approach, targeting successor root signing on a regular cadence to
support long-term PKI agility and risk reduction.

### Replacement Signing Cadence
New GoDaddy roots have a 15-year validity period with a long-term goal of targeting
successor root signing every four years to enable a future five-year root rotation model
for publicly trusted hierarchies.

### Cross-Signatures Between Generations
As this is a brand new VMC hierarchy with no predecessor root, there are no
cross-signatures in place or planned at this time.

### Trust Purposes
The GoDaddy Verified Mark Root CA - VMCR1 is scoped exclusively for the issuance of Mark Certificates. This root is not scoped for TLS
server authentication or any other trust purpose.

### Cryptographic Profiles
The VMCR1 root uses RSA 4096 with the SHA-256 signing algorithm. VMC intermediate
and subscriber certificates are signed using SHA-256. GoDaddy will continue to adopt
approved profiles and algorithms as appropriate as standards and root program
expectations evolve.

### Customer Transition Timeline
GoDaddy plans to begin live VMC certificate issuance from the VMCR1 hierarchy in
September 2026, subject to root store inclusion timing and operational readiness.
As this is a new hierarchy with no predecessor root, there is no subscriber migration
required from an existing hierarchy.

### Submission to Apple Root Program
New roots are submitted at the earliest opportunity after Root Generation Audit (RGA)
reports are finalized to allow sufficient review and distribution lead time ahead of
planned issuance.

### Removal of Deprecated Roots
As this is a new hierarchy, there are no deprecated roots associated with this request.
When future successor roots are introduced, deprecated roots will be retired after
subscriber transitions are complete. GoDaddy will coordinate timing with Apple to
minimize ecosystem impact and ensure timely removal.
