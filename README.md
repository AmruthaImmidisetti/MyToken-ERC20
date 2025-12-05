# MyToken (MTK) – ERC-20 Token Smart Contract

## 📌 Overview
MyToken (MTK) is a fully functional ERC-20 token implemented in Solidity and deployed using the Remix Ethereum IDE.  
This project demonstrates the core functionalities of an ERC-20 token, including balance tracking, token transfers, allowances, and event emission.

The goal of this project is to understand:
- How tokens work on Ethereum  
- How smart contracts function  
- How ERC-20 standards ensure compatibility with wallets and exchanges  
- How to test and deploy decentralized applications  

This project was completed as part of a blockchain learning assignment.

---

## 🚀 Features Implemented

### ✔️ Token Metadata
- **Name:** MyToken  
- **Symbol:** MTK  
- **Decimals:** 18  
- **Total Supply:** 1,000,000 MTK  

### ✔️ Core ERC-20 Functionalities
- `balanceOf(address)` – Returns balance of an address  
- `transfer(address to, uint256 value)` – Transfers tokens  
- `approve(address spender, uint256 value)` – Approve spender  
- `transferFrom(address from, address to, uint256 value)` – Transfer using allowance  
- `allowance(address owner, address spender)` – Returns approved spending amount  

### ✔️ Event Emission
- `Transfer` event  
- `Approval` event  

### ✔️ Validation & Security Checks
- Prevent transfers to zero address  
- Prevent transfers more than sender balance  
- Prevent spending without approved allowance  

### ✔️ Helper Functions
- `getTotalSupply()`  
- `getTokenInfo()`  

---

## 🛠️ Tools & Technologies Used
- **Solidity 0.8.x**
- **Remix Ethereum IDE**
- **Remix VM (JavaScript VM / Cancun VM)**
- **EVM (Ethereum Virtual Machine)**

---

## 📦 Total Supply Calculation
Since ERC-20 tokens use decimals, the total supply is: 1,000,000 MTK × 10^18 = 1000000000000000000000000 units

This value is passed as constructor input during deployment.

---

## 📥 Deployment Steps (Clear & Simple)

### 1️⃣ Open Remix IDE
Go to: https://remix.ethereum.org/

### 2️⃣ Create and Add Code
- Create `MyToken.sol` in **contracts/** directory  
- Paste the full MyToken contract code  

### 3️⃣ Compile
- Go to **Solidity Compiler**  
- Select version **0.8.x**  
- Click **Compile MyToken.sol**  

### 4️⃣ Deploy
- Go to **Deploy & Run Transactions**  
- Environment: **Remix VM (Cancun/JavaScript VM)**  
- In constructor input enter:  1000000000000000000000000
- Click **Deploy**

### 5️⃣ Test Functionality
- Call `name`, `symbol`, `decimals`, `totalSupply`  
- Check your balance with `balanceOf(deployerAddress)`  
- Transfer tokens using `transfer`  
- Approve another account using `approve`  
- Use `transferFrom` from spender’s account  
- Check allowances  
- Verify events in Remix logs  

---

## 🧪 Test Cases & Results

### ✔️ Transfer Test
- A → B  
- Balances updated  
- `Transfer` event emitted  

### ✔️ Approve Test
- A approves B  
- `Approval` event emitted  

### ✔️ transferFrom Test
- B transfers A’s tokens to C  
- Allowance reduced  
- `Transfer` event emitted  

---

## ❗ Edge Case Tests (All Required for Submission)

| Test Case | Expected Behavior | Result |
|----------|-------------------|--------|
| Transfer to zero address | Revert with error | ✅ Passed |
| Transfer more than balance | Revert with error | ✅ Passed |
| transferFrom without approval | Revert with error | ✅ Passed |

All failures show correct validation in the contract.

---

## 🖼️ Screenshots
All screenshots necessary for submission are included in the **/Screenshots** folder:

- Compilation success  
- Deployment success  
- Token metadata outputs  
- Transfer success  
- Approve success  
- transferFrom success  
- Event logs (Transfer/Approval)  
- Zero address transfer failure  
- Insufficient balance failure  
- Insufficient allowance failure  

---

## 📚 Learning Outcomes
From this project, I learned:

- Writing smart contracts in Solidity  
- How ERC-20 tokens operate at a low level  
- How approval and allowance mechanisms work  
- How to test transactions and analyze event logs in Remix  
- How blockchain state changes occur transparently  
- Best practices for validation and safety checks  

---

## 🏁 Conclusion
MyToken (MTK) is a fully working ERC-20 token smart contract that meets all standard requirements for academic and professional blockchain projects.  
The contract is secure, tested, validated, and compliant with ERC-20 interface standards.

This repository demonstrates strong understanding of:
- Solidity programming  
- Ethereum token standards  
- Smart contract deployment  
- Token economics  
