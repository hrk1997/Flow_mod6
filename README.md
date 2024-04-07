# Flow_mod6

# NFT-flow
This Cadence program implements the Non-Fungible Token standard for creating and managing the NFTs. 
This program allows users to mint new NFTs, deposit and withdraw NFTs, and transfer ownership of NFTs between different users.

## Description
A Cadence contract included in these files shows how to create and manage Non-Fungible Tokens (NFTs) on the Flow network using the standard NonFungibleToken library. The contract permits the development of NFTs that contain metadata like lucky number, favorite meal, and name. Along with these features, it allows you to borrow, transfer, withdraw, and deposit NFTs using a specific ID. The NonFungibleToken standard is implemented by the CryptoPoops contract, which also specifies a resource called NFT for the production of NFTs with customized information. Additionally, it defines a Collection resource that enables an address's NFT collection to be managed. A Minter resource for producing NFTs and minting them into a Collection is also included in the contract.


The public functions that can be used to interact with the Collection resource, including deposit, getIDs, borrowNFT, borrowAuthNFT, and withdraw, are defined by the CollectionPub interface. The functions createMinter and createEmptyCollection enable the construction of Minter resources for minting NFTs and empty collections, respectively.

Events are sent by the contract upon contract startup and upon NFT deposit and withdrawal. All things considered, this contract offers a straightforward NFT implementation and illustrates the fundamental features needed to create and administer NFTs in a blockchain setting.

## Requirements
* Access to a Flow network node.
* Cadence Compiler
* Cadence REPL
* Cadence SDK

#### Deploy the contract
* Compile the contract using the Cadence Compiler.
* Deploy the contracts "NonFungibleToken.cdc.cdc" and "NFT_1.cdc" to the Flow network node.(NOTE: deploying address should be updated on all required .cdc files) 
* Create the collection with "CreateColl.cdc"
* Mint a new NFT with "DepoNFT.cdc"
* Use Scripts to display metadata of the NFT's

#### Other Usable Functions Inside The Contract

* Withdraw an NFT

Call the getIDs() function on the Collection instance to get the list of NFT IDs you own.
Call the withdraw(withdrawID) function on the Collection instance and pass in the ID of the NFT you want to withdraw.
The NFT will be transferred back to the caller.

* Transfer an NFT

Call the borrowAuthNFT(id) function on the Collection instance and pass in the ID of the NFT you want to transfer.
Create a new instance of the Collection resource using the createEmptyCollection() function.
Call the deposit(token) function on the new Collection instance and pass in the borrowed NFT.
The NFT ownership will be transferred to the new Collection instance.

#### Reading NFT metadata
The following functions can be used to read NFT metadata:

* getIDs(): Returns the list of NFT IDs you own.
* borrowNFT(id): Returns a borrowed reference to an NFT by ID.
* borrowAuthNFT(id): Returns an authenticated borrowed reference to an NFT by ID.

The NFT resource defines the following fields:

* id: The unique identifier of the NFT.
* name: The name of the NFT.
* favouriteFood: The favourite food of the NFT.
* luckyNumber: The lucky number of the the NFT

## License
This NFT program is not licensed.
