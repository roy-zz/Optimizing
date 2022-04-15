### Security

#### Java 8

- Client-side TLS 1.2 enabled by default
- New variant of AccessController.doPrivileged that enables code to assert a subset of its privileges, without preventing the full traversal of the stack to check for other permissions
- Stronger algorithms for password-based encryption
- SSL/TLS Server Name Indication (SNI) Extension support in JSSE Server
- Support for AEAD algorithms: The SunJCE provider is enhanced to support AES/GCM/NoPadding cipher implementation as well as GCM algorithm parameters. And the SunJSSE provider is enhanced to support AEAD mode based cipher suites. See Oracle Providers Documentation, JEP 115.
- KeyStore enhancements, including the new Domain KeyStore type java.security.DomainLoadStoreParameter, and the new command option -importpassword for the keytool utility
- SHA-224 Message Digests
- Enhanced Support for NSA Suite B Cryptography
- Better Support for High Entropy Random Number Generation
- New java.security.cert.PKIXRevocationChecker class for configuring revocation checking of X.509 certificates
- 64-bit PKCS11 for Windows
- New rcache Types in Kerberos 5 Replay Caching
- Support for Kerberos 5 Protocol Transition and Constrained Delegation
- Kerberos 5 weak encryption types disabled by default
- Unbound SASL for the GSS-API/Kerberos 5 mechanism
- SASL service for multiple host names
- JNI bridge to native JGSS on Mac OS X
- Support for stronger strength ephemeral DH keys in the SunJSSE provider
- Support for server-side cipher suites preference customization in JSSE

#### Java 9

- JEP 219: Datagram Transport Layer Security (DTLS)
- JEP 244: TLS Application-Layer Protocol Negotiation Extension
- JEP 249: OCSP Stapling for TLS
- JEP 246: Leverage CPU Instructions for GHASH and RSA
- JEP 273: DRBG-Based SecureRandom Implementations
- JEP 288: Disable SHA-1 Certificates
- JEP 229: Create PKCS12 Keystores by Default
- JEP 287: SHA-3 Hash Algorithms

#### Java 10

- JEP 319: Root Certificates
- JDK-8148421: TLS Session Hash and Extended Master Secret Extension Support
- JDK-8186535: Removal of Deprecated Pre-1.2 SecurityManager Methods and Fields
- JDK-8148371: Removal of policytool
- JDK-8159544: Removal of Deprecated Classes in com.sun.security.auth.**
- JDK-8175091: java.security.{Certificate,Identity,IdentityScope,Signer} APIs Deprecated forRemoval
- JDK-8175094: java.security.acl APIs Deprecated forRemoval
- JDK-8159535: javax.security.auth.Policy API Deprecated forRemoval
- 