# 🚀 HTML Fund Me dApp

A simple frontend dApp that allows users to connect their wallet and interact with a **FundMe smart contract** (fund, withdraw, check balance).

This project is part of learning Web3 fundamentals — connecting frontend → wallet → smart contract.

---

## ⚡ Quickstart

### 1. Clone the repo
```bash
git clone https://github.com/Cyfrin/html-fund-me-cu
cd html-fund-me-cu
```

### 2. Run the app
- Open `index.html` directly in your browser  
OR
- Use VSCode Live Server extension (ritwickdey.LiveServer)

👉 You should see a **“Connect”** button

---

## 🔌 Connect Wallet

- Click **Connect**
- Approve connection in MetaMask

---

## 💻 Execute Transactions (Local EVM)

To interact with the contract (fund, withdraw), you need to deploy a smart contract locally.

---

# 🧱 Option 1: Foundry Setup

### Step 1: Clone backend repo
```bash
git clone https://github.com/Cyfrin/foundry-fund-me-cu
cd foundry-fund-me-cu
```

### Step 2: Build + start local chain
```bash
make build
make anvil
```

### Step 3: Deploy contract (new terminal)
```bash
make deploy
```

---

# ☕ Option 2: Moccasin Setup

### Step 1: Clone repo
```bash
git clone https://github.com/Cyfrin/buy-me-a-coffee-cu
cd buy-me-a-coffee-cu
```

### Step 2: Start local chain
```bash
anvil
```

### Step 3: Deploy contract (new terminal)
```bash
mox run deploy --network anvil
```

---

## 🔧 Configure Frontend

### 1. Update contract address

In `constants.js`:
```js
export const contractAddress = "YOUR_DEPLOYED_CONTRACT_ADDRESS";
```

👉 Copy this address from deployment output

---

### 2. Setup MetaMask

⚠️ IMPORTANT: Use a test account only

- Import one of the private keys from Anvil output  
- Add a custom network:

| Field | Value |
|------|------|
| Network Name | Localhost |
| RPC URL | http://127.0.0.1:8545 |
| Chain ID | 31337 |
| Currency | ETH |

---

## ▶️ Run the App

1. Refresh browser  
2. Click **Connect**  
3. Enter ETH amount  
4. Click **Fund**  

---

## 🧠 Features

- Connect wallet (MetaMask)  
- Fund contract with ETH  
- Withdraw funds (owner)  
- Get contract balance  

---

## ⚠️ Notes

- Always use test accounts  
- Never use wallets with real funds  
- Ensure MetaMask is connected to localhost (chainId 31337)  

---

## 📁 Project Structure

```
├── index.html        # UI
├── index.js          # Web3 logic
├── constants.js      # Contract address & ABI
```

---

## 🎯 Learning Goals

- Wallet connection (MetaMask)  
- Smart contract interaction (ethers.js)  
- Local blockchain setup (Anvil)  
- Frontend → blockchain integration  

---

## 🙌 Acknowledgements

- Cyfrin Web3 Course  
- Foundry Toolkit  
- Ethereum Ecosystem  

---

## 🚀 Next Improvements

- Add transaction status UI (loading/success/error)  
- Display wallet balance  
- Improve UI with React + Tailwind  
- Deploy to Sepolia testnet  
