# FAQ

### Frequently Asked Questions (FAQ)

> _This appendix answers common questions about the Digital Crypto Note (DCN) Standard. It is intended to help developers, enterprises, governments, manufacturers, publishers, merchants, investors, and end users better understand the goals, architecture, and practical implementation of the DCN ecosystem._

***

## Introduction

As a new open standard for **Physical Digital Assets**, DCN introduces concepts that combine blockchain, secure hardware, digital identity, payment systems, and cryptographic trust.

Many readers naturally ask similar questions regarding:

* What DCN is
* How it works
* How it differs from existing technologies
* Security
* Manufacturing
* Blockchain compatibility
* Governance
* Commercial opportunities

The following questions provide concise answers to the most common topics.

***

## General Questions

### What is the Digital Crypto Note (DCN)?

The Digital Crypto Note (DCN) Standard is an open technical standard for creating **Physical Digital Assets**.

It defines how secure physical devices can represent, protect, transfer, authenticate, and interact with blockchain-based assets and digital credentials.

***

### Is DCN a cryptocurrency?

No.

DCN is **not** a cryptocurrency.

It is an infrastructure standard that enables many different digital assets—including cryptocurrencies—to exist securely in physical form.

***

### Is DCN a blockchain?

No.

DCN does not replace blockchain networks.

Instead, it connects secure physical devices with blockchain infrastructure through standardized Blockchain Adapters.

***

### Is DCN a wallet?

No.

Wallets are applications that interact with DCN devices.

The DCN Standard defines the communication, ownership, security, and lifecycle of Physical Digital Assets—not a single wallet application.

***

## Technical Questions

### Does DCN require a specific blockchain?

No.

The DCN Standard is blockchain-neutral.

Compatible blockchain networks can integrate using the Blockchain Adapter SDK.

***

### Which blockchain networks are supported?

Potential supported networks include:

* Bitcoin
* Ethereum
* Polygon
* TON
* Solana
* Avalanche
* BNB Chain
* Hyperledger
* CBDC Networks
* Lycan Chain
* Future blockchain networks

Support depends on implementing a compatible Blockchain Adapter.

***

### Can DCN work offline?

Yes, depending on the deployment model.

Examples include:

* Offline authentication
* Offline identity verification
* Offline access control
* Offline credential validation
* Limited offline payment models with Publisher-defined risk policies

Final settlement or synchronization may still require connectivity depending on the asset type and Publisher rules.

***

### What communication technology does DCN use?

The primary communication technology is:

* NFC

Future implementations may also support:

* Bluetooth Low Energy (BLE)
* QR interoperability
* USB
* Secure wireless interfaces

***

## Security Questions

### How does DCN prevent counterfeiting?

DCN combines multiple security mechanisms including:

* Secure Elements
* Device Certificates
* Publisher Certificates
* Hardware Root of Trust
* Mutual Authentication
* Secure Messaging
* Cryptographic Challenge-Response
* Certificate Revocation

Authenticity is verified cryptographically rather than visually.

***

### What happens if a device is lost?

Recovery depends on Publisher policy.

Possible options include:

* Device replacement
* Ownership verification
* Asset migration
* Device revocation
* Replacement issuance

Some assets may intentionally be non-recoverable depending on their design.

***

### Can devices be cloned?

The DCN architecture is designed to make practical cloning significantly more difficult by relying on tamper-resistant hardware and cryptographic identities.

Security depends on the quality of the Secure Element, provisioning process, and implementation.

***

## Publisher Questions

### Who can become a Publisher?

Any organization meeting the technical, security, legal, and certification requirements defined by the DCN ecosystem may become a Publisher.

Examples include:

* Banks
* Governments
* Enterprises
* Universities
* Retailers
* Stablecoin Issuers
* Payment Companies
* Gaming Platforms
* Technology Companies

***

### What can Publishers issue?

Publishers may issue:

* Digital Cash
* Stablecoin Notes
* Gift Cards
* Payroll Assets
* Digital Identity
* Certificates
* Event Tickets
* Loyalty Assets
* Transit Cards
* Collectibles
* Future Physical Digital Assets

***

## Developer Questions

### Are SDKs available?

The roadmap includes official SDKs for:

* Wallets
* Publishers
* Merchants
* Verification Services
* Blockchain Adapters
* Manufacturing

Reference implementations and open-source libraries are expected to accompany future releases.

***

### Can developers build their own wallets?

Yes.

The DCN Standard encourages multiple independent wallet implementations.

Any wallet that follows the published specifications can interoperate with compliant Physical Digital Assets.

***

### Can developers build commercial products?

Yes.

The DCN Standard is intended to encourage commercial innovation while maintaining interoperability through open specifications and certification.

***

## Manufacturing Questions

### Who manufactures DCN devices?

Certified manufacturing partners produce DCN-compliant hardware according to the Secure Manufacturing and Provisioning standards defined by the ecosystem.

***

### What products can be manufactured?

Examples include:

* Digital Crypto Notes
* Smart Cards
* Metal Cards
* Identity Cards
* Gift Cards
* Wearables
* NFC Key Fobs
* Security Tokens
* Industrial Authentication Devices

***

## Enterprise Questions

### Can DCN integrate with existing enterprise systems?

Yes.

Publisher Platforms and Wallets can integrate with:

* ERP Systems
* CRM Platforms
* Identity Providers
* Payment Platforms
* HR Systems
* Government Services
* Banking Infrastructure

Standard APIs simplify integration.

***

### Can enterprises issue internal credentials?

Yes.

Possible enterprise applications include:

* Employee IDs
* Building Access
* Payroll
* Asset Tracking
* Equipment Authentication
* Professional Certifications

***

## Governance Questions

### Who owns the DCN Standard?

No single company owns the ecosystem.

The DCN Foundation serves as the steward of the open standard through transparent governance.

***

### Can the standard evolve?

Yes.

Future versions may introduce:

* New asset profiles
* New blockchain integrations
* New cryptographic algorithms
* Additional APIs
* New hardware capabilities
* Future identity standards

Backward compatibility remains an important design objective.

***

## Future Questions

### Is DCN limited to payments?

No.

Payments are only one application.

The architecture also supports:

* Identity
* Credentials
* Government Services
* Healthcare
* Transportation
* Education
* Loyalty
* Gaming
* Collectibles
* Enterprise Authentication
* Future Physical Digital Assets

***

### What is the long-term vision?

The long-term vision is to establish DCN as the **global open standard for Physical Digital Assets**, enabling trusted interaction between secure physical devices and digital infrastructure across governments, enterprises, financial institutions, and blockchain ecosystems.

***

## Quick Reference

```
Question                              Short Answer

Is DCN a blockchain?                  No

Is DCN a cryptocurrency?              No

Is DCN open?                          Yes

Can anyone build on DCN?              Yes

Does it support multiple blockchains? Yes

Does it require NFC?                  Primarily, yes

Can Publishers create products?       Yes

Can Wallets be independent?           Yes

Can Governments use DCN?              Yes

Can Enterprises adopt DCN?            Yes
```

***

## Final Thoughts

Every major technology standard begins with questions.

Questions lead to understanding.

Understanding leads to implementation.

Implementation leads to adoption.

The purpose of this FAQ is not only to answer common questions, but to encourage further discussion, experimentation, and collaboration.

As the DCN ecosystem evolves, this appendix will continue to grow alongside the standard.
