<div align="center">
<a href="https://github.com/goat-sdk/goat">
<img src="https://github.com/user-attachments/assets/5fc7f121-259c-492c-8bca-f15fe7eb830c" alt="GOAT" width="100px" height="auto" style="object-fit: contain;">
</a>
</div>

# Buy on Boson Protocol

This example demonstrates an AI agent that can query and purchase physical goods on [Boson Protocol](https://www.bosonprotocol.io/) — a trust-minimized commerce protocol.

The agent can browse offers, commit to purchases, and handle the full exchange lifecycle (redeem, complete, dispute) using its own EVM wallet.

## Setup

```bash
cp .env.example .env
# Fill in your keys
```

```
WALLET_PRIVATE_KEY=0x...   # Funded Polygon Amoy testnet wallet
OPENAI_API_KEY=sk-...
```

## Get a testnet wallet

```bash
node -e "
const {privateKeyToAccount, generatePrivateKey} = require('viem/accounts');
const pk = generatePrivateKey();
console.log('PK:', pk);
console.log('Address:', privateKeyToAccount(pk).address);
"
```

Fund it at [faucet.polygon.technology](https://faucet.polygon.technology) (select Amoy network).

## Run

```bash
pnpm install
pnpm ts-node index.ts
```

## Example prompts

- "Show me available offers on the testnet"
- "What products can I buy with USDC?"
- "Buy the cheapest available item"
- "Check the status of my exchanges"

<footer>
<br/>
<br/>
<div>
<a href="https://github.com/goat-sdk/goat">
  <img src="https://github.com/user-attachments/assets/59fa5ddc-9d47-4d41-a51a-64f6798f94bd" alt="GOAT" width="100%" height="auto" style="object-fit: contain; max-width: 800px;">
</a>
</div>
</footer>
