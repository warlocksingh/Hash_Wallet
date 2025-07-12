# HashWallet

MetaMask‑style **universal SHA‑256 wallet** for any Bitcoin‑family chain. Add a coin by entering its RPC URL—no forks needed.

## Features

* Import any SHA‑256 coin using RPC + chain info (like MetaMask custom networks)
* Works with UTXO coins (BTC, BCH, NMC, KAWRA, PEPE, etc.)
* Mobile-friendly wallet built with React Native
* Lightning Network support planned
* One-click APK build using EAS CLI

---

## ✅ Prerequisites

* Node.js ≥ **18.x** (you are currently on 12.x — update required!)
* Git installed
* `expo-cli` and `eas-cli` globally installed

### 🔧 Update Node.js on Ubuntu

```bash
sudo apt update
sudo apt install curl -y
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

Then verify:

```bash
node -v
npm -v
```

You should see Node.js ≥ 18.

---

## ⚙️ Setup Instructions

### 1. Clone the fixed repo:

```bash
cd ~
git clone https://github.com/warlocksingh/Hash_Wallet.git
cd Hash_Wallet
```

### 2. Clean and fix the SSH git dependency

```bash
nano package.json
```

Find this line:

```json
"react-native-ldk": "git@github.com:react-native-ldk/react-native-ldk.git"
```

Replace with:

```json
"react-native-ldk": "https://github.com/react-native-ldk/react-native-ldk.git"
```

Save and exit: `Ctrl+O`, `Enter`, then `Ctrl+X`

---

### 3. Install dependencies

```bash
rm -rf node_modules package-lock.json
npm install
expo install
```

### 4. Build APK (debug)

```bash
eas build -p android --profile preview --local
```

APK will be saved under `dist/` folder.

To generate production-signed AAB:

```bash
eas build -p android --profile production
```

---

## ✅ GitHub Repo

[https://github.com/warlocksingh/Hash\_Wallet](https://github.com/warlocksingh/Hash_Wallet)

---

Let me know if you need a pre-built APK or want a Lightning-only fork.
