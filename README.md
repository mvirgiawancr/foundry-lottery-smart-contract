# Foundry Smart Contract Lottery

This is a smart contract lottery project based on the Cyfrin Solidity Course, implementing a decentralized lottery system using Chainlink VRF for randomness and Chainlink Automation for automatic execution.

## 📌 Features

- Smart contract lottery system with Chainlink VRF integration
- Automated lottery draws using Chainlink Automation
- Comprehensive testing suite across multiple environments
- Gas-optimized contract deployment and verification
- Built with Foundry for robust Ethereum development

## 🚀 Getting Started

### 1. Install Requirements

Make sure you have installed:

- Git
- Foundry
- Optional: Gitpod for cloud development

### 2. Clone the Repository

```bash
git clone https://github.com/YourUsername/foundry-smart-contract-lottery.git
cd foundry-smart-contract-lottery
forge build
```

### 3. Configure Environment Variables

Create a `.env` file based on `.env.example`, then add:

```
SEPOLIA_RPC_URL=<your_rpc_url>
PRIVATE_KEY=<your_private_key>
ETHERSCAN_API_KEY=<your_etherscan_api_key>
```

## 🔧 Usage

### 1. Start a Local Node

```bash
make anvil
```

### 2. Deploy Smart Contract

For local deployment:

```bash
make deploy
```

For testnet deployment:

```bash
make deploy ARGS="--network sepolia"
```

### 3. Testing

Run various test suites:

```bash
# Local tests
forge test

# Forked network tests
forge test --fork-url $SEPOLIA_RPC_URL

# Test coverage
forge coverage
```

### 4. Chainlink Integration

#### Set up VRF Subscription

```bash
make createSubscription ARGS="--network sepolia"
```

#### Register Automation Upkeep

1. Visit automation.chain.link
2. Register new upkeep
3. Choose "Custom logic" as trigger mechanism
4. Configure your lottery contract address

## 📊 Scripts and Utilities

### Gas Estimation

```bash
forge snapshot
```

### Code Formatting

```bash
forge fmt
```

### Interact with Deployed Contract

```bash
cast send <LOTTERY_CONTRACT_ADDRESS> "enterLottery()" --value 0.1ether --private-key <PRIVATE_KEY> --rpc-url $SEPOLIA_RPC_URL
```

## 🔗 Dependencies

This project uses Chainlink's official contracts for VRF and Automation. The contracts are imported from the official Chainlink Brownie Contracts repository:

```bash
forge install smartcontractkit/chainlink-brownie-contracts@0.6.1 --no-commit
```

## 📜 License

This project is created for learning purposes and is free to use for further development.

## 💙 Thank You!

If you like this project, don't forget to ⭐ the repository on GitHub!

Made with 💖 by Virgi
