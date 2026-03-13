# NomaTab Voice

Voice-first credit ledger for informal merchants powered by BNB Chain.

---

## Overview

NomaTab Voice is a hackathon prototype that helps informal merchants track customer credit and build a verifiable financial history using blockchain.

Across many informal markets, merchants allow customers to buy goods on credit and record debts in handwritten notebooks. While this system works through trust, it creates problems:

- records can be lost
- debts can be disputed
- merchants have no digital financial history
- businesses cannot access financial services

NomaTab Voice digitizes the traditional tab book.

Merchants can record transactions using a voice-style interface and store a blockchain proof of each transaction on BNB Chain.

---

## Problem

Millions of small businesses track credit using notebooks like this:

Nomsa – R45  
Thabo – R120  
Sipho – R30  

These records are fragile and difficult to verify.

If the notebook is lost, the entire credit history disappears.

This leaves informal businesses without a financial identity.

---

## Solution

NomaTab Voice replaces the notebook with a digital credit ledger.

Example interaction:

Merchant says:

> "Add bread for Nomsa, fifteen rand on credit"

The system converts the voice command into structured transaction data and records the credit in a digital ledger.

Each transaction can generate a blockchain proof, creating a verifiable financial history.

---

## How It Works

1. Merchant records a credit sale
2. Voice input is converted into transaction data
3. The merchant ledger updates
4. A transaction proof is recorded on BNB Chain
5. Repayments update the customer balance

---

## Architecture

Merchant Interface  
↓  
Voice Processing  
↓  
Credit Ledger  
↓  
BNB Chain Smart Contract

---

## Smart Contract

The project includes a minimal Solidity smart contract that records credit transactions.

Example data stored:

- merchant name
- customer name
- transaction amount
- timestamp

---

## Demo Flow

The prototype demonstrates the following steps:

1. Merchant dashboard displays customer balances
2. Merchant records a credit sale
3. Voice-style command is parsed into transaction data
4. Blockchain proof is generated
5. Merchant records a repayment
6. Ledger updates balances

---

## Future Vision

NomaTab Voice is the first layer of the broader **Noma ecosystem**.

Future capabilities could include:

- merchant payments
- micro-loans
- inventory financing
- supplier networks
- digital commerce infrastructure
- local energy trading systems

---

## Project Status

Hackathon prototype.

The goal of this project is to demonstrate the concept of transforming informal credit transactions into verifiable digital financial identity.

---

## BNB Chain Integration

Smart contract will be deployed to BNB Chain testnet.

Contract Address:  
`TBD`

Transaction Hash 1:  
`TBD`

Transaction Hash 2:  
`TBD`

---

## Repository Structure
