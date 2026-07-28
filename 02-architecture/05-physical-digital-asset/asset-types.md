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
