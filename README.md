# One World Project

### Prize Pool

- Total Pool - $15,000
- H/M - $14,000
- Low - $1000

- Starts: November 06, 2024 Noon UTC
- Ends: November 13, 2024 Noon UTC

- nSLOC: 541

[//]: # (contest-details-open)

## About the Project

One World Project is a dynamic DAO marketplace where users can actively participate in decentralized organizations. This repository contains smart contracts for creating and managing DAO memberships using ERC1155 tokens. The contracts facilitate the creation and management of DAO memberships. Each DAO membership is represented by an ERC1155 token with different tiers.

Twitter: https://x.com/1W_Project

Website: https://www.oneworldproject.io/

## Actors

```text
Member: A user that has completed the signup and KYC process
DAO Creator: A user that creates a DAO
DAO Member: A user that holds a DAO's tokens. These users have the ability to make proposals for the DAO
```

[//]: # (contest-details-close)

[//]: # (scope-open)

## Scope (contracts)

#### Key Functionalities
​
MembershipFactory

- Create New DAO Membership: Deploys a new proxy contract for the DAO membership.
- Update DAO Membership: Updates the tier configurations for a specific DAO.
- Join DAO: Allows a user to join a DAO by purchasing a membership NFT at a specific tier.
- Upgrade Tier: Allows users to upgrade their tier within a sponsored DAO.
- Set Currency Manager: Updates the currency manager contract.
- Call External Contract: Allows the factory to perform external calls to other contracts.

 MembershipERC1155

- Initialize: Initializes the contract with the name, symbol, URI, and creator address.
- Mint Tokens: Mints new tokens.
- Burn Tokens: Burns existing tokens.
- Claim Profit: Allows users to claim profits from the profit pool.
- Send Profit: Distributes profits to token holders.
- Call External Contract: Allows the contract to perform external calls to other contracts.
​
```
All Contracts in `contracts` are in scope.
```
```js
├── OWPIdentity.sol
├── dao
│   ├── CurrencyManager.sol
│   ├── MembershipFactory.sol
│   ├── interfaces
│   │   ├── ICurrencyManager.sol
│   │   └── IERC1155Mintable.sol
│   ├── libraries
│   │   └── MembershipDAOStructs.sol
│   └── tokens
│       └── MembershipERC1155.sol
└── meta-transaction
      ├── EIP712Base.sol
      └── NativeMetaTransaction.sol
```

## Compatibilities

```
Compatibilities:
  Blockchains:
      - Polygon
  Tokens:
      - USDC
      - WETH
      - WBTC
```

[//]: # (scope-close)

[//]: # (getting-started-open)

​
### Prerequisites
​
- Node.js
- Hardhat
- Ethereum wallet (e.g., MetaMask)
- Access to an Ethereum node (e.g., Infura, Alchemy)

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/Cyfrin/2024-11-one-world.git
    ```

2. Install dependencies
    ```sh
    npm install
    ```

3. Test
    ```sh
    npx hardhat test
    ```


[//]: # (getting-started-close)
[//]: # (known-issues-open)

## Known Issues

[Cyfrin Private Audit Report](https://github.com/user-attachments/files/17599046/2024-10-29-one-world-project-v2.0.pdf)

**Additional known issues detected by LightChaser can be found [here](https://github.com/Cyfrin/2024-11-one-world/issues/1)

[//]: # (known-issues-close)
