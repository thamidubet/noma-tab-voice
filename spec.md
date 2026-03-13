# NomaTab Voice Hackathon Spec

## Project Name
NomaTab Voice

## One-line Pitch
NomaTab Voice is a voice-first credit ledger that helps informal merchants record customer tabs and turn everyday trust into verifiable financial identity on BNB Chain.

---

## Goal
Build a minimal hackathon-ready prototype for the BNB Chain hackathon.

The project should demonstrate how informal merchant credit transactions can be recorded digitally and verified using blockchain.

This is a prototype focused on storytelling and proof of concept rather than a production system.

---

## Core Concept

Across many informal markets, merchants track customer credit in handwritten notebooks.

Example:

Nomsa – R45  
Thabo – R120  
Sipho – R30  

These notebooks are fragile and difficult to verify. If the notebook is lost, the credit history disappears.

NomaTab Voice replaces the notebook with a digital ledger that allows merchants to record transactions quickly and optionally create a blockchain proof.

---

## Scope

Only build the minimum features required for a clear hackathon demonstration.

Required components:

1. Merchant dashboard showing customers and balances
2. New credit transaction flow
3. Voice-style transaction entry
4. Blockchain proof display
5. Repayment flow
6. Minimal Solidity smart contract
7. Clear README documentation
8. Demo-ready repository structure

---

## Non-Goals

Do NOT build the full Noma ecosystem.

Avoid implementing:

- full payment systems
- micro-loan engines
- inventory management
- complex speech recognition
- full authentication systems
- energy trading features
- advanced backend infrastructure

Focus only on the demo experience.

---

## Demo Flow

The prototype should support this user journey:

1. Merchant opens dashboard
2. Merchant sees existing customer tabs
3. Merchant taps "Record Sale"
4. Merchant enters or simulates voice input

Example voice command:

"Add bread for Nomsa, fifteen rand on credit"

5. App converts the command into structured data:

Customer: Nomsa  
Item: Bread  
Amount: 15  
Type: Credit

6. Merchant confirms the transaction

7. Transaction is recorded and a blockchain proof or transaction hash is displayed

8. Merchant can later record repayment

9. Ledger updates customer balance

---

## UX Requirements

The interface should remain simple and demo-friendly.

Suggested screens:

1. Dashboard
2. Voice Entry Screen
3. Blockchain Proof Screen
4. Repayment Screen

The goal is clarity for judges rather than visual perfection.

---

## Smart Contract Requirements

Create a minimal Solidity contract for BNB Chain testnet.

Suggested functionality:

- record credit transactions
- record repayments
- store merchant name
- store customer name
- store amount
- timestamp transactions

Example functions:

recordCredit(merchant, customer, amount)

recordRepayment(merchant, customer, amount)

Events may be emitted to help demonstrate transaction logging.

---

## Frontend Requirements

Use the fastest stack for a simple prototype.

Preferred stack:

- React + Vite
- basic CSS or Tailwind

The frontend should:

- display the merchant dashboard
- allow entry of new transactions
- simulate voice-style commands
- display blockchain proof
- show updated balances

No production-level design is required.

---

## Suggested Repository Structure

noma-tab-voice/

README.md  
spec.md  

frontend/  

smart-contract/  

assets/  

demo/

---

## README Requirements

README.md should include:

- project overview
- problem description
- solution explanation
- architecture diagram
- explanation of BNB Chain integration
- instructions for running the project
- future vision

Include placeholders for:

Contract Address  
Transaction Hash 1  
Transaction Hash 2  

---

## Definition of Done

The prototype is considered complete when:

- the repository structure exists
- the frontend runs locally
- the smart contract compiles
- the UI supports the demo flow
- the README explains the project clearly
- the project is demo-ready for a hackathon submission

---

## Priority

Prioritize:

clarity  
simplicity  
demo readiness  

over complexity or polish.

The objective is a convincing prototype demonstrating the concept.
