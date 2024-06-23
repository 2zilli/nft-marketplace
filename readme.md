# NFT Marketplace

Welcome to the NFT Marketplace coding task for Chromaway! This project demonstrates the basic functionality of a blockchain-based marketplace where users can register, create collections, mint NFTs, and more.

## Project Overview

This project is designed to showcase a basic implementation of an NFT marketplace using Rell, Chromia's blockchain language. It focuses on essential blockchain features such as user registration, token management, NFT minting, and marketplace operations. The implementation is kept minimal for clarity but follows best practices in code formatting, organization, and naming conventions.

## Functionality

The marketplace includes the following features:

-   **User Registration**: Users register with a public key, functioning as a whitelist. This can be extended to include KYC processes.
-   **Create Collection**: Users can create a new NFT collection.
-   **Mint NFT**: Users can mint a new NFT, either independently or as part of a collection.
-   **List NFT**: Users can list their NFTs for sale on the marketplace.
-   **Buy NFT**: Users can purchase listed NFTs, with balances and ownership transferred accordingly.
-   **Favorites Management**: Users can add or remove collections and NFTs from their favorites list.
-   **Token Management**: An admin can mint tokens, and users can transfer tokens between each other.

## Key Design Choices

-   **Public Key Authentication**: All users are registered with a public key, which simplifies authentication and ensures security. Each operation checks the signers to ensure the correct user is authenticated.
-   **Admin for Minting Tokens**: A designated admin (with a specific public key) is responsible for minting tokens. This ensures controlled token issuance.
-   **Fees**: While fees for operations are not implemented, the design includes placeholders and considerations for adding such features.
-   **Event Logging**: The project logs significant events like token transfers for transparency and auditability.

## How It Works

### User Registration

Users register by signing a transaction with their public key. This ensures only the legitimate owner of the corresponding private key can register.

### Creating Collections and Minting NFTs

Users can create collections and mint NFTs. Ownership is tracked using the owner's public key, and various checks ensure only the owner can manage their NFTs and collections.

### Listing and Buying NFTs

NFTs can be listed for sale, and buyers can purchase them using their token balances. Transactions ensure secure and atomic transfer of ownership and funds.

### Token Management

An admin can mint new tokens, and users can transfer tokens. The admin's public key is used to authenticate minting operations.

### Favorites Management

Users can add or remove NFTs and collections from their favorites, making it easy to track preferred items.

## Rell Code

The Rell code for this project ensures simplicity and readability. It includes unit tests to verify the functionality of each feature.

## Getting Started

### Materials

-   [Chromia Developer Tools](https://docs.chromia.com/)
-   [Chromia Learning Material](https://learn.chromia.com/)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/2zilli/nft-marketplace.git
    cd nft-marketplace
    ```

### Usage

The project includes several operations and queries to interact with the NFT marketplace. These can be tested and extended as needed to build a full-featured NFT marketplace on the blockchain.

## Tests

Rell unit tests are included to verify the functionality of the marketplace. These tests cover user registration, NFT minting, listing, purchasing, favorites management, and token management.

To run the tests, use the Chromia Developer Tools as outlined in the [Chromia Learning Material](https://learn.chromia.com/).
