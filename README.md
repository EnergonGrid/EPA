# Energon Project Adapter

**EPA · Energon Network Integration Layer**

The **Energon Project Adapter (EPA)** is the project-specific integration component created through the larger **Energon Network**.

EPA and Energon Network are closely related, but they are not the same contract. The Network is the deployed infrastructure; a Project Adapter is created for an individual project when it enters the Network.

---

## Purpose

The Energon Network provides the integration layer for projects and services that connect to the Energon ecosystem while keeping the Energon Core and EMP / EVault separate.

This layer covers:

- project onboarding
- Node creation
- Project Adapter creation
- Registry-linked services
- NFT delivery infrastructure
- service resolution
- Established Mark recognition
- permanent project payment records through EFlow

The integration layer does not rewrite Energon Core protocol rules or EMP / EVault economic rules.

---

## Mainnet Component Directory

The production integration stack is deployed on **Flare Mainnet — Chain ID 14**.

| Component | Version | Address |
| --- | --- | --- |
| Energon Network | v1.0.0 | `0x6c0bB202a4AF3126E21BbaD6c4D79A8DD41Cc5aC` |
| Energon Node Registry | v2.1.0 | `0x834F79cdDc43CF231bFe7b1abC622ceF7Cbe14a5` |
| Energon NFT System | v1.0.0 | `0xE542801A7F82c5E0D40a02e72EB5d40AB25C067c` |
| Energon NFT Delivery | v1.0.0 | `0xe946d9892E54A7F09e373894e8A478aa793bEcB0` |
| Energon Service Resolution | v1.0.0 | `0xE24b8f0D1a85b567b565322074A0f157EaE6053A` |
| Energon Established Mark | v1.0.0 | `0x28525B92678Bd3AFA5825b45421842bfA46DFdBa` |

These addresses identify distinct contracts with separate responsibilities. The table should not be interpreted as meaning every component has the same authority or permissions.

---

## Network and Project Adapter Relationship

The current architecture follows this model:

- `EnergonNetwork` is the deployed Network contract.
- A project enters the Network through `EnergonNetwork.createNode()`.
- The entry process creates that project's **Energon Project Adapter**.
- There is **no single standalone global EPA Mainnet address**.
- Each Project Adapter address must be obtained from the real Node creation transaction, emitted events, and current on-chain state.

The Solidity contract retains the name **`EnergonProjectAdapter`**.

---

## Separation of Responsibility

**Energon Core**
- Energon Token (EON)
- EnergonCube
- EnergonController
- Guardian coherence and deterministic protocol progression

**EMP / EVault**
- reserves
- economic eligibility
- claims
- maturity
- payout controls
- economic safeguards

**EPA / Energon Network**
- project integration
- Nodes
- Project Adapters
- Registry-linked services
- NFT delivery
- service resolution
- network recognition

These layers interact without being interchangeable.

---

## Repository Scope

This repository is the dedicated home for the production Energon Project Adapter / Energon Network integration system.

Planned repository material includes:

- verified production Solidity source
- production ABIs
- Flare Mainnet deployment records
- `createNode()` documentation
- Project Adapter discovery and lifecycle
- Node Registry integration
- NFT Delivery and Service Resolution documentation
- Established Mark documentation
- EFlow documentation
- verified Mainnet testing and transaction records

Production source files will only be added from the verified artifacts used for the live contracts.

---

## Interfaces and Documentation

Main Energon overview:

**https://github.com/EnergonGrid/EnergonGrid**

Energon Management Protocol / EVault:

**https://github.com/EnergonGrid/Energon-Management-Protocol**

Energon DApp:

**https://github.com/EnergonGrid/energon-dapp**

---

## Source of Truth

If this repository, an interface, or any other description differs from the deployed implementation, the **deployed contracts and live blockchain state control actual execution**.

Documentation explains the architecture. It does not override contract law.

---

**EnergonGrid · Flare Mainnet**
