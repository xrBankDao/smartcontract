# xrBankDAO: The Liquidity Layer for XRP EVM-Sidechain

XrBankDAO was created to provide stablecoin liquidity to the emerging XRPL EVM sidechain, fostering growth within the ecosystem. Additionally, it was developed to enable XRP holders who supply liquidity to utilize their assets more efficiently and, if needed, to use stablecoins with low volatility.

## Why xrBankDAO?

XRPL’s DeFi ecosystem holds tremendous potential. In the Korean market alone, over 8 billion XRP are held on centralized exchanges (CEX, upbit/bithumb), with more than 2 million holders. However, the DeFi market remains relatively undeveloped.

Moving forward, XRPL plans to launch its own fiat-backed stablecoin and an EVM sidechain. However, relying solely on bridged fiat-backed stablecoins introduces risks such as volatility of backing assets, bridge vulnerabilities, and supply shortages.

We are committed to filling this crucial gap by introducing a robust, crypto-backed stablecoin that will serve as the foundation for XRPL’s DeFi ecosystem. This stablecoin will not only enhance the security and stability of the network but also provide XRP holders with new opportunities to earn yield and participate in decentralized finance. Our vision is to unlock the full potential of XRPL’s DeFi capabilities, ensuring that it becomes a leading player in the global blockchain economy.

---

## System Design Diagrams and Narrative

### System Design Overview

xrBankDAO’s architecture follows a decentralized model to maintain security and reliability. The core contracts handle collateral, stablecoin issuance, yield generation, and liquidation if necessary. The primary components include:

- **Vault**: Manages collateral deposits, mints stablecoins, and ensures solvency.
- **Minting**: Allows users to mint stablecoins (XSD) against their deposited XRP collateral.
- **Earnings**: Users can earn yield by providing liquidity or through interest-bearing features on XSD.

![System Diagram](./Modules.png)

## xrBankDao Smart Contract

MarkerDao Forked Project.

contract Address in educhain testnet is in below.

vat : 0x514066e1f24fDA9f2B379748f9C001C3475625cB  
gem : 0x345E902846aC3805719483d80D664ABa0B6aF40C  
gemJoin : 0xD40588c705B99d406B048629E4D8863a2434beF5  
esd : 0xCef966528A867176BF3a575c9951f695e8eB77a3  
esdJoin : 0x42FfAe0648A84c0AC72D012402f380ab511AcBb1  
jug : 0x09Fd469b3036E45Dad077Df411134Fb85218678e  
spot : 0x92B7e50CE799e8E26dE7324b3a92e93Dbbdf554F  
abacus : 0x4529d97aEfAF713E5bB20635f3C6b4Ac48175fC2  
clip :0xc1bb3FA0431a9ab7d490dA1e2fb5B693d1178FF8  
dog : 0x4011fC8085497b72f0287CBB0BcDa853ea07263b  
flap : 0x95Fb13b7ffd5F55F2D78c26700E16a262aC2EeF8  
flop : 0xf9b7Bbfc5E2acA9a168a50E1807F7903c2f2dF0D  
vow : 0xC913B2Aad7F11404E4E91E53f2388f760F5A3AfA  
pot : 0x07964F526825fcdCd54DdEd9aeE063bbb6968517  
flash : 0x03e8DaF83b6fEc6c7a1cCA35FD8Aa73A48480F64  
cdpManager : 0x0E492702CA0A2048e87A21CE3Ac7E11Be757af2b  
...

## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
