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

#### Java 11

- JDK-8240256: New SunPKCS11 Configuration Properties
- JDK-8225083: Removed Google's GlobalSign Root Certificate
- JDK-8225082: Removed IdenTrust Root Certificate
- JDK-8163326: Updated the Default Enabled Cipher Suites Preference
- JDK-8238555: SunPKCS11 Initialization With NSS When External FIPS Modules Are in Security Modules Database
- JDK-8076190: Customizing PKCS12 keystore Generation
- JDK-8243559: Removed Root Certificates with 1024-bit Keys
- JDK-8225081: Removed Telia Company's Sonera Class2 CA Certificate
- JDK-8153005: Upgraded the Default PKCS12 Encryption and MAC Algorithms
- JDK-8254631: Improve Encoding of TLS Application-Layer Protocol Negotiation (ALPN) Values
- JDK-8244473: New System and Security Properties to Control Reconstruction of Remote Objects by JDK's Built-in JNDI RMI and LDAP Implementations
- JDK-8256421: Added 2 HARICA Root CA Certificates
- JDK-8202343: Disable TLS 1.0 and 1.1
- JDK-8213400: -groupname Option Added to keytool Key Pair Generation
- JDK-8206925: Support for certificate_authorities Extension
- JDK-8252226: Support for X25519 and X448 in TLS
- JDK-8218021: jarsigner Preserves POSIX File Permission and symlink Attributes
- JDK-8233228: Weak Named Curves in TLS, CertPath, and Signed JAR Disabled by Default
- JDK-8245417: Improve Certificate Chain Handling
- JDK-8172404: Tools Warn If Weak Algorithms Are Used
- JDK-8243320: Added 3 SSL Corporation Root CA Certificates
- JDK-8243321: Added Entrust Root Certification Authority - G4 certificate
- JDK-8242141: New System Properties to Configure the TLS Signature Schemes
- JDK-8231507: Apache Santuario Library Updated to Version 2.1.4
- JDK-8225069: Removal of Comodo Root CA Certificate
- JDK-8225068: Removal of DocuSign Root CA Certificate
- JDK-8237474: Default SSLEngine Should Create in Server Role
- JDK-8210985: Default SSL Session Cache Size Updated to 20480
- JDK-8026953: Support for MS Cryptography Next Generation (CNG)
- JDK-8200400: Allow SASL Mechanisms to Be Restricted
- JDK-8080462: SunPKCS11 Provider Upgraded with Support for PKCS#11 v2.40
- JDK-8230318: New Checks on Trust Anchor Certificates
- JDK-8227758: Exact Match Required for Trusted TLS Server Certificate
- JDK-8232019: dded LuxTrust Global Root 2 Certificate
- JDK-8233223: Added 4 Amazon Root CA Certificates
- JDK-6913047: Memory Growth Issue in SunPKCS11 Fixed
- JDK-8148188: New Java Flight Recorder (JFR) Security Events
- JDK-8228825: Remove Obsolete NIST EC Curves from the Default TLS Algorithms
- JDK-8218723: Use SunJCE Mac in SecretKeyFactory PBKDF2 Implementation
- JDK-8219013: Updated XML Signature Implementation to Apache Santuario 2.1.3
- JDK-8224499: System Property jdk.security.useLegacyECC is Turned Off by Default
- JDK-8223499: Removal of Two DocuSign Root CA Certificates
- JDK-8222136: Removal of Two Comodo Root CA Certificates
- JDK-8222137: Removal of T-Systems Deutsche Telekom Root CA 2 Certificate
- JDK-8195793: Removal of GTE CyberTrust Global Root
- JDK-8219013: com.sun.org.apache.xml.internal.security.ignoreLineBreaks System Property
- JDK-8217763: System Property to Switch Between Implementations of ECC
- JDK-8216577: Added GlobalSign R6 Root Certificate
- JDK-8207258: Distrust TLS Server Certificates Anchored by Symantec Root CAs
- JDK-8210432: Added Additional TeliaSonera Root Certificate
- JDK-8261624: Problem looking up Client Certificates in keystore
- JDK-8208350: Disabled All DES TLS Cipher Suites
- JDK-8201756: mproved Cipher Inputs

#### Java 12 
 
- JDK-8223499: Removal of Two DocuSign Root CA Certificates
- JDK-8222136: Removal of Two Comodo Root CA Certificates
- JDK-8222137: Removal of T-Systems Deutsche Telekom Root CA 2 Certificate
- JDK-8216577: Added GlobalSign R6 Root Certificate
- JDK-8191053: disallow and allow Options for java.security.manager System Property
- JDK-8213400: -groupname Option Added to keytool Key Pair Generation
- JDK-8148188: New Java Flight Recorder (JFR) Security Events
- JDK-8076190: Customizing PKCS12 keystore Generation
- JDK-8140466: ChaCha20 and Poly1305 TLS Cipher Suites
- JDK-8195793: Removal of GTE CyberTrust Global Root
- JDK-8210432: Added Additional TeliaSonera Root Certificate
- JDK-8203230: Removal of AOL and Swisscom Root Certificates
- JDK-8213363: Change to X25519 and X448 Encoded Private Key Format
- JDK-8214140: Removed TLS v1 and v1.1 from SSLContext Required Algorithms
- JDK-8211883: Disabled TLS anon and NULL Cipher Suites
- JDK-8208350: Disabled All DES TLS Cipher Suites
- JDK-8207258: Distrust TLS Server Certificates Anchored by Symantec Root CAs

#### Java 13

- JDK-8191808: Configurable Read Timeout for CRLs
- JDK-8219861: New keytool -showinfo -tls Command for Displaying TLS Configuration Information
- JDK-8026953: Support for MS Cryptography Next Generation (CNG)
- JDK-8080462: SunPKCS11 Provider Upgraded with Support for PKCS#11 v2.40
- JDK-8171279: Support for X25519 and X448 in TLS
- JDK-8211018: Session Resumption without Server-Side State in JSSE
- JDK-8200400: Allow SASL Mechanisms to Be Restricted
- JDK-8224767: New String Constants for Canonical XML 1.1 URIs
- JDK-8223053: [xmldsig] Added KeyValueEC_TYPE
- JDK-8223172: Support for Kerberos Cross-Realm Referrals (RFC 6806)
- JDK-8222137: Removal of T-Systems Deutsche Telekom Root CA 2 Certificate
- JDK-8223499: Removal of Two DocuSign Root CA Certificates
- JDK-8222136: Removal of Two Comodo Root CA Certificates
- JDK-8215430: Removal of the Internal com.sun.net.ssl Package Only Used for Compatibility with Legacy JSSE 1.0 Applications
- JDK-8217835: Removal of Experimental FIPS 140 Compliant Mode from SunJSSE Provider
- JDK-8160247: Deprecated javax.security.cert APIs with forRemoval=true
- JDK-8218723: Use SunJCE Mac in SecretKeyFactory PBKDF2 Implementation
- JDK-6913047: Memory Growth Issue in SunPKCS11 Fixed
- JDK-8163326: Updated the Default Enabled Cipher Suites Preference
- JDK-8168261: Use Server Cipher Suites Preference by Default
- JDK-8219013: Updated XML Signature Implementation to Apache Santuario 2.1.3
- JDK-8225748: javap Checksum Uses SHA-256

#### Java 14

- JDK-8225069: Removal of Comodo Root CA Certificate
- JDK-8225068: Removal of DocuSign Root CA Certificate
- JDK-8237474: Default SSLEngine Should Create in Server Role
- JDK-8233228: Weak Named Curves in TLS, CertPath, and Signed JAR Disabled by Default
- JDK-8231507: Apache Santuario Library Updated to Version 2.1.4
- JDK-8191138: Removed Deprecated java.security.acl APIs
- JDK-8214024: Removal of the Default keytool -keyalg Value
- JDK-8234924: Deprecated the Legacy Elliptic Curves for Removal
- JDK-8234870: Deprecated the OracleUcrypto JCE Provider for Removal
- JDK-8227758: Exact Match Required for Trusted TLS Server Certificate
- JDK-8230318: New Checks on Trust Anchor Certificates
- JDK-8232019: Added LuxTrust Global Root 2 Certificate
- JDK-8233223: Added 4 Amazon Root CA Certificates
- JDK-8233016: Protected javax.crypto.Cipher Constructor Throws IAE for Non-null Invalid Arguments
- JDK-8180392: SunJCE Provider Throws NoSuchAlgorithmException for AES/GCM/PKCS5Padding
- JDK-8228825: Remove Obsolete NIST EC Curves from the Default TLS Algorithms
- JDK-8190492: Removed SSLv2Hello and SSLv3 From Default Enabled TLS Protocols
- JDK-8228396: Stateless Resumption Enabled by Default for JSSE Server
- JDK-8231196: DelegationPermission Allows Creating an Instance That Thows NPE on equals Call

#### Java 15

- JDK-8245417: Improve Certificate Chain Handling
- JDK-8243320: Added 3 SSL Corporation Root CA Certificates
- JDK-8243321: Added Entrust Root Certification Authority - G4 certificate
- JDK-8242060: Added Revocation Checking to jarsigner
- JDK-8172404: Tools Warn If Weak Algorithms Are Used
- JDK-8172680: SunJCE Provider Supports SHA-3 Based Hmac Algorithms
- JDK-8242141: New System Properties to Configure the TLS Signature Schemes
- JDK-8206925: Support for certificate_authorities Extension
- JDK-8225069: Removal of Comodo Root CA Certificate
- JDK-8225068: Removal of DocuSign Root CA Certificate
- JDK-8241039: Retired the Deprecated SSLSession.getPeerCertificateChain() Method Implementation
- JDK-8219989: Removal of com.sun.net.ssl.internal.ssl.Provider Name
- JDK-8237219: Disabled Native SunEC Implementation by Default
- JDK-8242260: Added forRemoval=true to Previously Deprecated ContentSigner APIs
- JDK-8243424: Signature and SignatureSpi Get Parameter Methods May Return null When Unsupported
- JDK-8237474: Default SSLEngine Should Create in Server Role

#### Java 16

- JDK-8225081: Removed Telia Company's Sonera Class2 CA certificate
- JDK-8256421: Added 2 HARICA Root CA Certificates
- JDK-8242068: Signed JAR Support for RSASSA-PSS and EdDSA
- JDK-8172366: SUN, SunRsaSign, and SunEC Providers Supports SHA-3 Based Signature Algorithms
- JDK-8218021: jarsigner Preserves POSIX File Permission and symlink Attributes
- JDK-8244148: Added -trustcacerts and -keystore Options to keytool -printcert and -printcrl Commands
- JDK-8242332: SunPKCS11 Provider Supports SHA-3 Related Algorithms
- JDK-8245417: Improve Certificate Chain Handling
- JDK-8254631: Improve Encoding of TLS Application-Layer Protocol Negotiation (ALPN) Values
- JDK-8166596: TLS Support for the EdDSA Signature Algorithm
- JDK-8243559: Removed Root Certificates with 1024-bit Keys
- JDK-8235710: Removal of Legacy Elliptic Curves
- JDK-8241003: Deprecated the java.security.cert APIs That Represent DNs as Principal or String Objects
- JDK-8243320: Added 3 SSL Corporation Root CA Certificates
- JDK-8243321: Added Entrust Root Certification Authority - G4 certificate
- JDK-8153005: Upgraded the Default PKCS12 Encryption and MAC Algorithms
- JDK-8202343: Disable TLS 1.0 and 1.1