# Asset Types

The DCN Standard defines a set of standardized asset profiles that specify how a Physical Digital Asset behaves. These profiles ensure interoperability across wallets, merchants, issuers, and blockchain networks while allowing publishers to implement different business models.

Every DCN-compliant asset shall conform to one of the following standardized profiles or an approved future extension.

***

### DCN-S — Stored Value

**Purpose**

DCN-S represents a fixed-value digital asset intended to function similarly to physical cash.

The value is loaded during issuance and remains fixed until spent or redeemed.

#### Characteristics

* Fixed denomination
* Cryptographically secured
* Transferable
* Supports offline verification (implementation dependent)
* Simple payment experience
* Minimal user interaction

#### Example Values

* 10 USDT
* 20 USDT
* 50 USDT
* 100 USDT
* 500 USDT
* 1,000 USDT

#### Typical Use Cases

* Digital cash
* Retail payments
* Gift cards
* Emergency funds
* Humanitarian aid

***

### DCN-R — Reloadable

**Purpose**

DCN-R represents a reusable Physical Digital Asset whose balance can increase or decrease over time.

Unlike DCN-S, the denomination is not fixed.

#### Characteristics

* Reloadable balance
* Multiple transactions
* Long operational life
* Wallet pairing supported
* Balance synchronization
* Spending history

#### Typical Use Cases

* Personal crypto wallet
* Payroll cards
* Student cards
* Transit wallets
* Family allowance cards

***

### DCN-P — Programmable

**Purpose**

DCN-P extends the reloadable model by supporting programmable rules enforced by publishers or smart contracts.

#### Supported Rules

* Spending limits
* Merchant restrictions
* Geographic restrictions
* Daily transaction limits
* Time-based validity
* Expiration dates
* Multi-signature approval
* Corporate policy enforcement

#### Typical Use Cases

* Employee expense cards
* Government subsidy programs
* Travel allowances
* Educational grants
* Corporate treasury
* Enterprise payments

***

### DCN-C — Collectible

**Purpose**

DCN-C represents collectible Physical Digital Assets where authenticity, rarity, and provenance are primary characteristics.

A collectible may optionally contain transferable digital value.

#### Characteristics

* Limited edition
* Serial numbering
* Cryptographic provenance
* Ownership history
* Optional stored value
* Authenticity verification

#### Typical Use Cases

* Limited edition Digital Crypto Notes
* Sports memorabilia
* Event collectibles
* Museum artifacts
* NFT-linked physical assets
* Commemorative issues

***

## DCN-D — Digital Draft

**DCN-D (Digital Draft)** is a fully funded, cryptographically verifiable digital payment instrument designed to bring the concept of a traditional bank Demand Draft into the digital asset economy.

A traditional Demand Draft allows a payer to provide funds to a bank and receive a payment instrument that represents guaranteed value. The recipient does not need to trust the payer personally because the instrument can be independently verified and is backed by funds already provided by the purchaser.

DCN-D applies a similar principle to digital assets.

Instead of asking a recipient to trust:

* a wallet screenshot,
* a transaction screenshot,
* an unknown token,
* an exchange balance,
* a counterparty,
* or an intermediary,

the recipient can independently verify the Digital Draft against the DCN Protocol.

The underlying digital asset is locked before the DCN-D is issued.

Therefore, a valid DCN-D represents **verifiable locked value rather than a promise to pay later**.

### Core Principle

A DCN-D follows a simple principle:

> **Lock first. Verify independently. Settle later.**

The payer deposits an approved digital asset into the DCN settlement infrastructure.

The protocol locks the specified amount and generates a unique Digital Draft.

The draft can then be presented to another person or organization.

The recipient does not need to understand wallets, private keys, blockchain explorers, or token contracts to determine whether the payment instrument is genuine.

They can verify it through a DCN-compatible verification interface.

***

### Example

Alice wants to pay Bob **10,000 USDT**.

Bob does not normally accept cryptocurrency.

Alice creates:

**DCN-D #DCN-8F92-71K**

The protocol locks:

**Asset:** USDT\
**Network:** Ethereum\
**Amount:** 10,000 USDT\
**Status:** FUNDED\
**Beneficiary:** Bob\
**Issuer:** Alice\
**Settlement Status:** Unredeemed

Alice can provide Bob with a physical DCN-D, QR code, NFC instrument, printable document, or digital draft reference.

Bob visits a DCN verification interface and enters or scans the Draft ID.

The interface independently reads the state of the relevant DCN smart contracts.

Bob can verify that:

**10,000 USDT actually exists and is locked for this Digital Draft.**

He is therefore verifying the underlying value rather than trusting Alice's representation of it.

***

## Why DCN-D Exists

Crypto payments currently assume that both participants understand cryptocurrency.

In the real world, this is frequently not true.

A person receiving payment may:

* not have a crypto wallet,
* not know how wallets work,
* not understand blockchain networks,
* not know how to verify a token contract,
* fear fake or imitation tokens,
* fear manipulated screenshots,
* fear fraudulent transactions,
* prefer fiat settlement,
* or simply not want custody of cryptocurrency.

DCN-D separates **receiving value** from **understanding crypto infrastructure**.

The recipient only needs to understand:

> "This instrument represents verified value that has already been locked."

***

#### Use Case 1 — Paying Someone Who Does Not Understand Crypto

Consider a crypto holder who needs to make a large payment to a person who does not normally use cryptocurrency.

The recipient may refuse USDT because they do not know:

* which wallet to install,
* which blockchain to use,
* whether the token is genuine,
* whether the transaction can be trusted,
* or how the asset will eventually be converted into fiat.

Instead of transferring crypto directly, the payer creates a DCN-D.

#### Flow

```
PAYER
  │
  │  Deposits Digital Asset
  ▼
DCN-D SMART CONTRACT
  │
  │  Locks Funds
  ▼
DIGITAL DRAFT CREATED
  │
  │
  ├──────────────► Draft ID
  ├──────────────► QR
  ├──────────────► NFC
  └──────────────► Printable Instrument
                         │
                         ▼
                    RECIPIENT
                         │
                         │ Verify
                         ▼
                 DCN VERIFICATION
                         │
                         ▼
               FUNDS CONFIRMED
                         │
                         ▼
               ACCEPT DIGITAL DRAFT
                         │
                ┌────────┴────────┐
                ▼                 ▼
          CRYPTO WALLET      SETTLEMENT
                              PROVIDER
                                  │
                                  ▼
                                FIAT
```

The recipient can independently confirm:

* Draft ID
* asset
* blockchain
* token contract
* amount
* funding status
* issuer
* beneficiary
* creation time
* expiry conditions
* redemption status

No blockchain knowledge should be required from the recipient.

***

#### Use Case 2 — OTC Crypto Trading

Large peer-to-peer and OTC cryptocurrency transactions frequently suffer from a fundamental problem:

**Who moves first?**

The buyer may not want to send fiat before receiving crypto.

The seller may not want to send crypto before receiving fiat.

Both parties may also worry about:

* fake balances,
* fake transaction screenshots,
* imitation tokens,
* unverified assets,
* counterparty identity,
* settlement failure,
* source-of-funds concerns,
* and untrusted escrow intermediaries.

DCN-D can provide a new settlement primitive for such transactions.

#### Example

A buyer wants to purchase:

**500,000 USDT**

Instead of attempting to prove ownership using screenshots or wallet balances, the seller creates:

**DCN-D — 500,000 USDT**

The underlying 500,000 USDT is locked by the protocol.

When the buyer meets the seller, the seller presents the Draft ID.

The buyer independently verifies:

```
Draft
DCN-D #8F92-71K

Asset
USDT

Amount
500,000

Status
FUNDED

Issuer
Verified

Beneficiary
Buyer / Agreed Recipient

Redeemed
NO
```

The parties can therefore begin settlement knowing that the digital asset side of the transaction has already been cryptographically committed.

DCN-D does not eliminate the need for appropriate compliance, legal agreements, or fiat-side settlement controls.

It instead removes an important uncertainty:

> **Does the seller actually control the crypto being offered for settlement?**

***

#### Use Case 3 — Alternative Digital Asset Custody Model

Some users are uncomfortable maintaining significant balances inside conventional wallets.

Their concerns may include:

* losing a seed phrase,
* losing a password,
* device theft,
* phishing,
* signing malicious transactions,
* wallet compromise,
* exchange account restrictions,
* or accidental transfers.

DCN-D introduces another way of representing access to locked digital value.

Instead of keeping the asset continuously available inside a general-purpose wallet, a user may create one or more Digital Drafts.

For example:

```
User Assets
│
├── DCN-D #001 → 10,000 USDT
├── DCN-D #002 → 25,000 USDT
├── DCN-D #003 → 50,000 USDT
└── DCN-D #004 → 100,000 USDT
```

Each draft represents independently verifiable locked value.

However, DCN-D should **not be presented as eliminating custody risk entirely**.

It changes the security model.

The DCN Protocol must therefore define secure mechanisms for:

* ownership authentication,
* beneficiary assignment,
* recovery,
* cancellation,
* redemption,
* lost physical instruments,
* compromised credentials,
* and dispute handling.

***

## Named Digital Draft

DCN-D should support a **Named Draft**.

A Named Draft is payable only to a specified beneficiary.

For example:

```
Issuer:
Alice

Beneficiary:
Bob

Asset:
USDT

Amount:
100,000

Status:
FUNDED
```

The draft cannot simply be taken by another person and redeemed.

The beneficiary identity is cryptographically associated with the instrument.

Depending on implementation, beneficiary identity could be represented through:

* wallet address,
* Decentralized Identifier (DID),
* verified identity hash,
* institutional account,
* settlement provider identifier,
* or another DCN-approved identity mechanism.

Sensitive personal information should not be placed directly on a public blockchain.

***

## Transferable Digital Draft

The standard may optionally support transferable DCN-D instruments.

For example:

```
Alice
  │
  ▼
Creates DCN-D
  │
  ▼
Bob
  │
  │ Endorses / Transfers
  ▼
Charlie
  │
  ▼
Redeems
```

Every transfer would update the recognized beneficiary or ownership state.

This creates the possibility of digitally endorsed payment instruments while maintaining an auditable chain of ownership.

Transferability should be configurable because some regulatory or commercial applications may require drafts to remain non-transferable.

***

## DCN-D State Model

A Digital Draft should have an explicit lifecycle.

```
CREATED
   │
   ▼
FUNDED
   │
   ▼
ISSUED
   │
   ▼
PRESENTED
   │
   ▼
ACCEPTED
   │
   ▼
REDEEMED
```

Alternative states may include:

```
CANCELLED

EXPIRED

FROZEN

DISPUTED

REFUNDED
```

The exact availability of these states depends on the implementation and applicable rules.

***

## Proof of Funds

One of the most important properties of DCN-D is **Proof of Funds**.

A valid draft must not merely state:

> 100,000 USDT

The DCN infrastructure must be capable of proving that the corresponding amount is actually locked or otherwise committed according to the settlement protocol.

Conceptually:

```
DCN-D
   │
   ▼
Draft Registry
   │
   ▼
Settlement Contract
   │
   ▼
Locked Asset
   │
   ▼
100,000 USDT
```

Therefore:

**Draft Value ≤ Verifiably Locked Value**

A draft cannot be legitimately issued without the corresponding backing required by its settlement model.

***

## Verification

Every DCN-D should be independently verifiable.

A user may:

1. Scan the QR code.
2. Tap the NFC instrument.
3. Enter the Draft ID.
4. Open a DCN-compatible verification application.

The verifier then retrieves the authoritative draft state.

Example:

```
DIGITAL CRYPTO NOTE

DCN-D

DIGITAL DRAFT

✓ AUTHENTIC

500,000 USDT

Status
FUNDED

Beneficiary
VERIFIED

Underlying Asset
VERIFIED

Redeemed
NO

Settlement
AVAILABLE
```

The verification interface is only a presentation layer.

The authoritative state should ultimately derive from the protocol and its settlement infrastructure rather than from a screenshot or manually entered database record.

***

## Redemption

A recipient should have multiple settlement possibilities.

#### Crypto Redemption

The beneficiary provides a compatible wallet address.

```
DCN-D
   ↓
Beneficiary Authentication
   ↓
Settlement Contract
   ↓
USDT
   ↓
Beneficiary Wallet
```

#### Exchange Redemption

A participating exchange may accept the DCN-D and credit the beneficiary's account after completing its required verification and compliance procedures.

#### Fiat Settlement

An authorized third-party settlement provider may accept the DCN-D and provide the beneficiary with fiat settlement subject to applicable regulation, compliance, fees, and banking arrangements.

Therefore, someone can potentially receive value represented by a DCN-D without personally managing the underlying cryptocurrency throughout the entire process.

***

## Physical DCN-D

DCN-D can exist digitally or be represented through a physical instrument.

A physical Digital Draft could contain:

* DCN-D identifier
* QR verification code
* NFC interface
* secure element
* issuer information
* beneficiary reference
* denomination
* asset symbol
* network reference
* cryptographic authentication
* anti-counterfeit printing
* serial number
* security markings

The physical document itself does not create the value.

> **The protocol state creates the value; the physical draft represents access to and verification of that state.**

Counterfeiting the printed instrument therefore cannot create additional underlying funds.

***

## Privacy

DCN-D must balance transparency with financial privacy.

Public verification should reveal only information necessary to establish authenticity.

For example:

```
Amount          ✓
Asset           ✓
Funding         ✓
Draft Status    ✓
Beneficiary     Verified
Issuer          Verified
```

It should not automatically expose:

```
Full Legal Name
Home Address
Government ID
Phone Number
Complete Transaction History
Other Wallet Balances
```

Identity claims can instead be represented through cryptographic attestations, DIDs, zero-knowledge mechanisms, or regulated verification providers.

***

## Security Principle

DCN-D changes the trust model from:

```
TRUST THE PERSON
```

to:

```
VERIFY THE INSTRUMENT
        +
VERIFY THE FUNDS
        +
VERIFY THE BENEFICIARY
        +
VERIFY THE SETTLEMENT STATE
```

This is the fundamental purpose of the Digital Draft standard.

***

## DCN-D vs Traditional Demand Draft

| Traditional Demand Draft             | DCN-D Digital Draft                             |
| ------------------------------------ | ----------------------------------------------- |
| Issued through financial institution | Issued through DCN-compatible infrastructure    |
| Fiat-backed                          | Digital-asset-backed                            |
| Bank verifies funds                  | Protocol verifies committed funds               |
| Physical instrument                  | Physical or digital instrument                  |
| Bank verifies authenticity           | Cryptographic verification                      |
| Bank settlement                      | Smart-contract / settlement-provider settlement |
| Banking hours may apply              | Protocol verification can operate continuously  |
| Usually jurisdiction-specific        | Designed as an interoperable technical standard |

DCN-D is inspired by the economic concept of a Demand Draft but does not claim to be legally equivalent to a bank-issued Demand Draft.

The legal classification of a DCN-D may differ between jurisdictions.

***

## DCN Family

With the introduction of DCN-D, the Digital Crypto Note family becomes:

| Type      | Name          | Primary Purpose                      |
| --------- | ------------- | ------------------------------------ |
| **DCN-S** | Stored Value  | Fixed-value digital cash             |
| **DCN-R** | Reloadable    | Reusable physical digital wallet     |
| **DCN-P** | Programmable  | Rule-based digital value             |
| **DCN-C** | Collectible   | Collectible + digital value          |
| **DCN-D** | Digital Draft | Verifiable funded payment instrument |

Each type solves a different interaction between physical instruments, digital ownership, and blockchain-based value.

DCN-D specifically addresses the **trust and settlement problem**.

***

## Design Objective

The long-term objective of DCN-D is simple:

> **Allow someone who does not understand cryptocurrency to confidently receive cryptocurrency-backed value without needing to trust the person giving it to them.**

The recipient should not need to ask:

**"Can I trust you?"**

They should be able to ask:

**"Can I verify the draft?"**

And the DCN Protocol should provide the answer.

## Industry-Specific Implementations

The standardized profiles above can be adapted for different industries without changing the DCN protocol.

| Industry                          | Typical Profile |
| --------------------------------- | --------------- |
| Digital Crypto Notes              | DCN-S, DCN-R    |
| Stablecoin Cards                  | DCN-R           |
| CBDCs                             | DCN-S, DCN-R    |
| Government Identity               | DCN-P           |
| Employee Badge                    | DCN-P           |
| Transit Card                      | DCN-R           |
| Event Ticket                      | DCN-P           |
| Gift Card                         | DCN-S           |
| Membership Card                   | DCN-R           |
| Healthcare Card                   | DCN-P           |
| Student Card                      | DCN-R           |
| Hotel Key                         | DCN-P           |
| Digital Passport                  | DCN-P           |
| Collectible Notes                 | DCN-C           |
| Tokenized Real Estate Certificate | DCN-C           |
| Demad Draft                       | DCN-D           |

***

## Future Profiles

The DCN Standard is designed to evolve.

Future standardized profiles may include:

* DCN-I — Identity
* DCN-T — Ticketing
* DCN-M — Machine Identity
* DCN-A — Autonomous AI Agent
* DCN-X — Custom Extension

These profiles are reserved for future versions of the specification and do not form part of DCN Specification v1.0.
