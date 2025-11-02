# Contributing to XPLA Smart Contract Tutorials

Thank you for your interest in contributing!  

## Guidelines

1. Fork the repository and clone it locally.
2. Create a branch for your feature or bugfix:
```bash
   git checkout -b feature/my-feature
```

3. Make your changes.
4. ChatGPT dapat membuat kesalahan. Periksa info penting. Lihat Preferensi Cookie.
```bash
git add .
git commit -m "Add new feature"
```
5. Push your branch:
```bash
git push origin feature/my-feature
```

6. Open a Pull Request and describe your changes.
### 4️⃣ examples/deploy.sh
```bash
#!/bin/bash

# 🚀 Simple deployment script for my_xpla_contract

WALLET="mytestwallet"
NODE="https://cube-rpc.xpla.dev"
CHAIN_ID="cube_47-5"
WASM_FILE="../artifacts/my_xpla_contract.wasm"
FEES="600000000000000000axpla"
GAS="2000000"

xplad tx wasm store $WASM_FILE \
  --from $WALLET \
  --gas $GAS \
  --fees $FEES \
  --node $NODE \
  --chain-id $CHAIN_ID \
  -y
