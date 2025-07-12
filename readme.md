# HashWallet

MetaMask‑style **universal SHA‑256 wallet** for any Bitcoin‑family chain. Add a coin by entering its RPC URL—no forks needed.

## Quick Start

```bash
# clone & install deps
npm install -g expo-cli eas-cli
expo install

# run in Expo Go
expo start
```

## Build APK

```bash
eas build -p android --profile preview --local  # debug APK
eas build -p android --profile production       # signed AAB/APK in cloud
```

See `App.js` for the one‑file React Native implementation.

