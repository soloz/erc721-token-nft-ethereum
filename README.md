## Simple ERC721 Non-fungible Token (NFT) Service for Animals using Ethereum Solidity

The project demonstrates a siimple Non-fungible Token (NFT) use case that allows tokens to be minted into an address and made available for viewinig via a simple UI. The NFT mintinig service [1] generates an NFT of an animal into an address on a local blockchain (hardhat) node and stores the NFT image of the anima along with its metadata in an Interplanetary File Service (IPFS), a decentralised file system on the web.

An existiing, archiived service [1] was leveraged in creating this project.

## Installation:

Follow the installation guide in the minty folder observing some slight changes below.

1. Start ipfs daemon with `ipfs daemon` or use tthe automatically started IPFS desktop
2. Change http://localhost:5001 to http://127.0.0.1:5001 in minty/default.json
3. Ensure `npx hardhat noode` binds to hostname 127.0.0.1:8545 and not ::1:8545 (or use `npx hardhat node --hostname 127.0.0.1`)
4. If `./start-local-environment.sh` doesn't work, then start the node manually with `npx hardhat node`
5. Compile contract with: `npx hardhat compile`
6. Change name and symbol of the nint from JLP using command `minty deploy -o minty-deployment.json -n SolContract -s SOLC`

The project demos a simple workflow of the following

1. NFT mint (via the `mint` command provided by [1])
   Mintng a Wolf NFT:
   ![Alt text](image.png)

2. NFT import into metamask (not required for listiing)
   Import Wolf NFT in metamask:
   ![Alt text](image-1.png)

3. Listing of the NFTs into a simple web UI
   ![Alt text](image-2.png)

[1] https://github.com/yusefnapora/minty
