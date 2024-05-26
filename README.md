
![Logo](https://taikai.azureedge.net/wYRAkDMmVjO-LIHBDG0TTa0v6CcZEYFPXNGxrKF170w/rs:fit:350:0:0/aHR0cHM6Ly9zdG9yYWdlLmdvb2dsZWFwaXMuY29tL3RhaWthaS1zdG9yYWdlL2ltYWdlcy80ZDg5MmI5MC0xYjdhLTExZWYtOGVmMy04NWY0ZTdiZGIxYTdDYXB0dXJlIGTigJllzIFjcmFuIDIwMjQtMDUtMjYgYcyAIDE4LjA5LjAxLnBuZw)

# VARA COLORS

VARA Colors is a project made during [Polkadot Prodigy Hackaton.](https://www.polkadotprodigy.com/)
It's a collection of non-fungible tokens living entirely on the VARA blockchain. Contrary to regular NFTs, there is no metadata off-chain as all their attributes are living on the blockchain, in the program's state.

NFT from Vara Colors don't need a server to be displayed. They question what an image *is* and what defines the *uniqueness* of a token.

The idea behind this project was to experiment with the [VARA blockchain](https://vara.network/developers), which enables smart-contracts to be created in Rust. Thanks to its technology, each NFT is unique and permanent.

## Features

- Choose a text for your NFT
- Choose a text color mode (black, white, vara)
- Choose a saturation value (0-100) for the background
- Choose a light value (0-100) for the background
- Mint your NFT (free on testnet)
- Transfer your NFT
- Burn your NFT

## Screenshots

![App Screenshot](https://storage.googleapis.com/taikai-storage/images/279cb970-1b79-11ef-8ef3-85f4e7bdb1a7varaColors.png)

![Demo 1](https://storage.googleapis.com/taikai-storage/images/dbef7810-1b81-11ef-8ef3-85f4e7bdb1a7vr1.png)

![Demo 2](https://storage.googleapis.com/taikai-storage/images/e6611d30-1b81-11ef-bba9-4b1cc9a55ddavr2.png)

![Demo 3](https://storage.googleapis.com/taikai-storage/images/ea402c20-1b81-11ef-84ff-45573b110433vr3.png)

## Demo

- You can access to the front-end [here.](https://vara-colors.vercel.app/)
- You can access to the program [here.](https://idea.gear-tech.io/programs/0xacf1987d2e17008191fa792e1b695d53170b6072d0418932ec12f090cd34892a?node=wss%3A%2F%2Ftestnet.vara.network)
- You can access to the smart-contract code [here.](https://github.com/mar1/Vara-Colors/blob/main/contracts/nft/src/lib.rs)
- You can access to the Taikai project homepage [here.]()

## Tech Stack

**Client:** Vue, Nuxt, TailwindCSS

**Server:** Node, Vercel

**Blockchain:** Gear-js, Vara staging network

## Roadmap

- Create the proof-of-concept ✅

- Fix the problem with webpack, Nuxt and gear-api on Vercel

- Deploy contract on VARA Network (main-net)

- Add a gallery of Vara Colors already mined

- Transform the collection into a DAO: the VARA collected will go to secure the chain, and the rewards will be passed on to the NFT holders, in proportion to those they own.

## Optimizations

Unfortunately, there seems to be a problem between Vercel, gear-api, Nuxt and webpack that is hindering deployment. Although the code works locally, the deployed front-end doesn't allow the transaction to be launched. However, the code is available as a comment on github and works locally.

## Authors

- [@mar1dev](https://www.github.com/mar1)

## Acknowledgements

- [November Font](https://www.1001fonts.com/november-font.html) by Tepid Monkey Fonts
- [gNFT Standard](https://wiki.gear-tech.io/docs/examples/Standards/gnft-721)
