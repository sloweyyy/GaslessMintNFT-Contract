# Trustify Smart Contract

This repository contains the smart contract for the Trustify platform. This contract is responsible for creating and managing the NFTs that represent notarized documents on the platform.

## GaslessMintNFT Contract

The core of this project is the `GaslessMintNFT.sol` smart contract. This contract allows for the creation of NFTs in a "gasless" manner for the end-user, which is a critical feature for the Trustify platform to provide a seamless user experience.

### Features

*   **ERC721 Compliant:** The contract is fully compliant with the ERC721 standard, ensuring that the NFTs are interoperable with other platforms and wallets.
*   **Gasless Minting:** The contract uses OpenZeppelin's `ERC2771Context` to enable gasless transactions. This means that a trusted forwarder can pay for the gas fees on behalf of the user, who can then mint NFTs without needing to hold any cryptocurrency.
*   **Ownable:** The contract is `Ownable`, meaning that there is an owner who has administrative privileges, such as setting the trusted forwarder.

## Setup

This project is designed to be used with the [Remix IDE](https://remix.ethereum.org/). To get started, simply open the project in Remix.

## Compilation and Deployment

To compile and deploy the contract, follow these steps:

1.  **Open the project in Remix.**
2.  **Compile the `GaslessMintNFT.sol` contract.**
3.  **Deploy the contract.** When deploying, you must provide the address of a trusted forwarder in the constructor. This is a crucial step for the gasless minting feature to work correctly.

    For example, if you are using a local Ganache instance for testing, you would deploy the contract with the address of one of your Ganache accounts as the `trustedForwarder`.

## Testing

The project includes a test file, `MyToken_test.sol`, which can be used to test the contract's functionality. To run the tests, simply open the test file in Remix and run the tests.

## Technologies Used

*   [Solidity](https://soliditylang.org/)
*   [OpenZeppelin Contracts](https://openzeppelin.com/contracts/)
*   [Remix IDE](https://remix.ethereum.org/)
*   [Ethers.js](https://ethers.io/)
*   [Web3.js](https://web3js.org/)
