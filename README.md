## ERC721MC

ERC721MC is a modification of the ERC721M to include the creator token contracts (https://github.com/limitbreakinc/creator-token-contracts) and their programmable royalty extensions.

Both token types share a common base token standard (the Azuki ERC721A), so this is essentially adding the necessary code to bridge the functionality of the Magic Eden ERC721M's minting stages, merkel-root based security, cosigning, etc. with Limit Break's ERC721AC behaviors. 

Ideally, the ERC721MOperatorFiltererRoyaltySplitter.sol will serve as a reference for implementing creator-minter shared royalties within the framework of the Magic Eden ERC721MOperatorFilterer.

Additional hardhat tests have been added to demonstrate the compatibility and functionalities of this variation. 

## ERC721M

ERC721M is a EVM minting protocol that enables the multi stage minting, per stage WL management, per stage supply limit, and crossmint support.

## Motivation

We'd like to introduce the standard of "minting stages". At each stage, the creators can define the following properties:

- per-stage price
- per-stage walletLimit
- per-stage merkleRoot
- per-stage maxStageSupply

The composability of the stages is generic enough to enable flexible and complicated EVM minting contracts.

![](https://bafkreid7sfgi5tycdvbdtobl3mqnwjlrlawdgioaj6vxvtcmmda74doh7q.ipfs.nftstorage.link/)


## Build status
![github ci status](https://github.com/magiceden-oss/erc721m/actions/workflows/ci.yml/badge.svg?branch=main)

![npm](https://img.shields.io/npm/v/@magiceden-oss/erc721m?color=green)


## Tech/framework used

<b>Built with</b>
- [hardhat](https://hardhat.org)
- [ERC721A](https://github.com/chiru-labs/ERC721A), ERC721M is based on the popular ERC721A contract.

## Features

- Minting Stages
- Permenent BaseURI Support
- Non-incresing Max Total Supply Support
- Per-stage WL Merkle Tree
- Per-stage Max Supply
- Global and Per-stage Limit
- Native TypeScript and Typechain-Types Support

## Installation
Provide step by step series of examples and explanations about how to get a development env running.


```bash
npm add @magiceden-oss/erc721m
```

## Code Example

```typescript
import { ERC721M, ERC721M__factory } from '@magiceden-oss/erc721m';

const contract = ERC721M__factory.connect(
  contractAddress,
  signerOrProvider,
);
```

## API Reference

```bash
# Compile the contract
npm run build

# Get the auto generated typechain-types
./typechain-types
```

## Tests

```bash
npm run test
```

We are targeting 100% lines coverage.

![](https://bafkreic3dyzp5i2fi7co2fekkbgmyxgv342irjy5zfiuhvjqic6fuu53ju.ipfs.nftstorage.link/)

## Security
- [ERC721M Kudelski Security Audit](./docs/AUDIT-PUBLIC-RELEASE-MagicEden-ERC721M1.pdf)
- Hacker One Bounty Program, please contact https://magiceden.io/.well-known/security.txt

## Used By

- [Magic Eden Launchpad](https://magiceden.io/launchpad/about)

## License

MIT © [MagicEden Open Source](https://github.com/magiceden-oss)

