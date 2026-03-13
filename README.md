# noma-tab-voice

## Repository Review

Current status:
- No Solidity source files are present yet (`.sol` not found in this repo).
- No deployment scripts/configs are present yet.

To submit to a BNB Chain hackathon, add your contract file(s) and follow the BNB testnet readiness checklist below.

## 1) Solidity contract suitability for BNB Chain Testnet

Use this checklist to verify your contract is compatible with **BNB Chain Testnet (chainId: 97)**:

- ✅ Solidity version is modern and explicit (recommended: `pragma solidity ^0.8.20;` or similar 0.8.x).
- ✅ No chain-specific assumptions for Ethereum-only precompiles or L2-only opcodes.
- ✅ Uses standard EVM patterns (OpenZeppelin libraries are fine).
- ✅ Constructor arguments and access controls are clearly defined.
- ✅ Gas-heavy loops are avoided for user-triggered functions.
- ✅ Revert messages and events are included for debugging and demo clarity.
- ✅ Contract compiles cleanly in Remix/Hardhat/Foundry.

BNB Chain Testnet RPC examples:
- `https://data-seed-prebsc-1-s1.bnbchain.org:8545`
- `https://bsc-testnet.public.blastapi.io`

Explorer:
- `https://testnet.bscscan.com`

## 2) Deployment instructions (BNB Chain Testnet)

### Option A: Remix (quickest for hackathon demo)
1. Open Remix IDE: `https://remix.ethereum.org`.
2. Add your Solidity contract file (for example, `NomaTabVoice.sol`).
3. Compile with a matching Solidity compiler version.
4. Open **Deploy & Run Transactions**.
5. Set environment to **Injected Provider - MetaMask**.
6. In MetaMask, switch to **BNB Chain Testnet** (chainId 97).
7. Ensure wallet has test BNB from a faucet.
8. Deploy contract.
9. Copy deployed contract address from Remix/MetaMask.
10. Verify deployment transaction on BscScan testnet.

### Option B: Hardhat (scriptable)
1. Install dependencies:
   ```bash
   npm install --save-dev hardhat @nomicfoundation/hardhat-toolbox dotenv
   ```
2. Configure `hardhat.config.js` with BNB testnet network:
   ```js
   require("dotenv").config();
   require("@nomicfoundation/hardhat-toolbox");

   module.exports = {
     solidity: "0.8.20",
     networks: {
       bscTestnet: {
         url: "https://data-seed-prebsc-1-s1.bnbchain.org:8545",
         chainId: 97,
         accounts: [process.env.PRIVATE_KEY]
       }
     }
   };
   ```
3. Add a deploy script (`scripts/deploy.js`) and run:
   ```bash
   npx hardhat run scripts/deploy.js --network bscTestnet
   ```
4. Save deployed address and tx hash in the placeholders below.

## 3) How to produce two successful transactions

After deployment, execute two state-changing methods so you can show on-chain activity.

Example flow:
1. **Tx #1 (deployment)**
   - Deploy contract to BNB testnet.
   - Confirm tx success on BscScan.
2. **Tx #2 (interaction)**
   - Call any write function (e.g., `setMessage("hello bnb")`, `mint(...)`, `register(...)`, depending on your contract).
   - Confirm success on BscScan.

Recommended evidence for submission:
- BscScan link to contract address.
- BscScan link to deployment tx.
- BscScan link to at least one successful interaction tx.
- Optional screenshot/video of contract UI interaction.

## 4) Hackathon submission placeholders

Fill these before submitting:

- **Contract Address (BNB Testnet):** `0x________________________`
- **Deployment Tx Hash:** `0x________________________`
- **Interaction Tx Hash #1:** `0x________________________`
- **Interaction Tx Hash #2 (optional but recommended):** `0x________________________`

BscScan links template:
- `https://testnet.bscscan.com/address/0x________________________`
- `https://testnet.bscscan.com/tx/0x________________________`
- `https://testnet.bscscan.com/tx/0x________________________`
