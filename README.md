# SkylineProbe

Built for Base

SkylineProbe is a lightweight Base-first repository built to confirm wallet onboarding, chainId correctness, and basic onchain reads on Base networks using official Coinbase tooling.

It is intentionally minimal and is best used as a quick, repeatable check for Base RPC availability and explorer visibility.

## Networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

## What It Does

Primary file: app/skylineProbe.ts

When executed, the application:
- Initializes an OnchainKitProvider for the selected Base chain
- Displays OnchainKit wallet connection UI
- Uses Viem to read Base state:
  - RPC chainId
  - latest block number
  - native ETH balance for a supplied address
- Surfaces Basescan references for manual inspection

## Repository Layout

app/  
- skylineProbe.ts  
  React entry component wiring OnchainKit wallet UX with Base JSON-RPC reads.

Common supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx

## Tooling

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base RPC reads  

## Installation and Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run using a standard React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## Author

GitHub: https://github.com/payday-sepia

Public contact (email): 0.payday_sepia@icloud.com

Public contact (X): https://x.com/stacey_mat63366

## License

MIT License

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xb1c084245a8f6f108cf5f971474d6de5e0f23fa1  

Deployment and verification:
- https://sepolia.basescan.org/address/0xb1c084245a8f6f108cf5f971474d6de5e0f23fa1  
- https://sepolia.basescan.org/0xb1c084245a8f6f108cf5f971474d6de5e0f23fa1 /0#code  

Contract #2 address:  
0xc3a4434def220a9213c5d5f29800cc22c0d3787f

Deployment and verification:
- https://sepolia.basescan.org/address/0xc3a4434def220a9213c5d5f29800cc22c0d3787f
- https://sepolia.basescan.org/0xc3a4434def220a9213c5d5f29800cc22c0d3787f/0#code  

Contract #3 address:  
0xeb0255c4b87702fb780095445c306d688cdb85d4

Deployment and verification:
- https://sepolia.basescan.org/address/0xeb0255c4b87702fb780095445c306d688cdb85d4  
- https://sepolia.basescan.org/0xeb0255c4b87702fb780095445c306d688cdb85d4/0#code 

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
