## GoDaddy CA Lifecycle Management

### Active Roots in Operation

| Root Common Name                              | crt.sh                                               | Not After   | Key Algorithm | Key Size | Signing Algorithm |
| ---                                           | ---                                                  | ---         | ---           | ---      | ---               |
| Go Daddy Root Certificate Authority - G2      | [crt.sh 548406](https://crt.sh/?id=548406)           | 2037-12-31  | RSA           | 2048     | SHA-256           |
| Starfield Root Certificate Authority - G2     | [crt.sh 221795](https://crt.sh/?id=221795)           | 2037-12-31  | RSA           | 2048     | SHA-256           |

### Successor Roots

| Root Common Name            | crt.sh                                                   | Not After   | Key Algorithm | Key Size | Signing Algorithm | Notes |
| ---                         | ---                                                      | ---         | ---           | ---      | ---               | ---   |
| GoDaddy TLS Root CA - R1    | [crt.sh 20878431179](https://crt.sh/?id=20878431179)     | 2040-08-24  | RSA           | 4096     | SHA-256           | Successor signed ahead of G2 2037 expiry; inclusion in progress. R1 root and intermediates use SHA-256 signature algorithm. |
| Starfield TLS Root CA - R1  | [crt.sh 20878454206](https://crt.sh/?id=20878454206)     | 2040-08-23  | RSA           | 4096     | SHA-256           | Successor signed ahead of G2 2037 expiry; inclusion in progress. R1 root and intermediates use SHA-256 signature algorithm. |

### Replacement Signing Cadence

New GoDaddy roots have a 15-year validity period with a long-term goal of targeting successor root signing every four years to enable a future 5-year root rotation for the WebPKI.

### Cross-Signatures Between Generations

GoDaddy’s G2 roots have cross-signed the new R1 successors to ensure path continuity during migration. Cross-signatures are limited in scope and duration to reduce chain complexity while enabling smooth subscriber transitions.

All R1 roots and their intermediate certificates are signed with the SHA-256 signature algorithm.

| Common Name                 | crt.sh                                               | Not After   | Key Algorithm | Key Size | Signing Algorithm | Notes                                                |
| ---                         | ---                                                  | ---         | ---           | ---      | ---               | ---                                                  |
| GoDaddy TLS Root CA - R1    | [crt.sh 21408225576](https://crt.sh/?id=21408225576) | 2040-08-24  | RSA           | 4096     | SHA-256           | Cross-signed by Go Daddy Root Certificate Authority - G2 |
| Starfield TLS Root CA - R1  | [crt.sh 21408224860](https://crt.sh/?id=21408224860) | 2040-08-23  | RSA           | 4096     | SHA-256           | Cross-signed by Starfield Root Certificate Authority - G2 |

### Trust Purposes

Both GoDaddy G2 and Starfield G2 are scoped for TLS server authentication (DV, OV, EV). The separate chains serve distinct customer segments and have been in continuous operation since 2009.

### Cryptographic Profiles

Active G2 roots use RSA. Successor R1 roots use RSA-4096. All R1 root and intermediate certificates use the SHA-256 signing algorithm. Subscriber certificates are issued with RSA 2048 or RSA 4096 keys. We will adopt approved profiles and algorithms as appropriate.

### Customer Transition Timeline

The G2 to R1 transition is planned for approximately four months. This rotation removes the ClientAuth EKU from subscriber certificates, and we are operationalizing transitions to accelerate future rotations.

### Submission to Apple Root Program

New roots are submitted at the earliest opportunity after Root Generation Audit (RGA) reports are finalized to allow sufficient review and distribution lead time.

### Removal of Deprecated Roots

Deprecated roots can be removed after subscriber transitions are complete. We will coordinate timing with Apple to minimize ecosystem impact and ensure timely removal.


