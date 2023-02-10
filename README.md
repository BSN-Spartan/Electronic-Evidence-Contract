## Electronic Evidence

Electronic evidence is a means used to preserve evidence, and there are many scenarios. For example, in the copyright field, authors can save their work fingerprints to an e-evidence service agent, and when a copyright dispute arises, it can be resolved through forensics. The key link of deposition and forensics is the e-evidence service agent. How to ensure its trustworthiness, that is, will the agent itself damage the deposition data? The traditional centralized agent is difficult to solve this problem. Now, it can be solved by blockchain technology. In the blockchain technology, the electronic ledger is jointly maintained by various nodes, and its content is determined by the consensus algorithm, and a single node cannot tamper with the ledger data that has reached consensus. This tamper-proof feature is the core of the decentralized e-evidence solution. In this application, the deposited data is no longer stored in a single institution, but is distributed and stored on all blockchain nodes.

## Prerequisite

Before using a smart contract, it is important to have a basic understanding of Ethereum and Solidity.   


## Overview

Electronic evidence is a way to record the whole process of "user identity verification, data creation, storage and transmission", and apply a series of security technologies to ensure the authenticity, integrity and security of electronic data in all aspects, which has complete legal effect in justice.

The use of blockchain and smart contract for data deposition has the following advantages:

 - Tamper-proof mechanism: The use of blockchain technology strengthens the tamper-proof nature of evidence.
 - Recognition: Judicial institutions, as nodes on the chain, are involved in recognizing and signing the data on the chain, and the true validity of the data can be confirmed from the chain afterwards.
 - Effectiveness: After the data is committed to the chain by consensus, even if some validator nodes withdraw, it will not cause the data to be lost or invalidated.

## Usage

The use of this application is as follow: 
Create a deposition -> Store a deposition -> Withdraw a deposition.

 - Creator: the creator of the evidence submits the deposition to the chain. The system data, online signed contracts, documents and bills, as well as the process data of the parties' willingness to act can be deposited through digital certificates, time stamps and other technical means, and then generate a unique hash value.
 - Storage party: save the deposited data. In this application, the smart contract on the blockchain acts as the storage party.
 - User: extract the deposited data. When the certificate is on the chain, the user can check the certificate owner, timestamp and other related information for verification at any time.


## Main Functions

### setData

```
 setData(bytes32 hash, address owner, bytes memory remarks, uint timestamp)
```

The creator submits the request. "hash" is the summary of the deposited data, "owner" is the attribution, "remarks" is the description, and "timestamp" is the effective time stamp.
        

### getData

```  
getData(bytes32 hash) public view returns(bytes32 , address, bytes memory, uint)
```

The user can get the evidence data. 

## License

Spartan-Electronic-Evidence Contract is released under the [Spartan License](https://github.com/BSN-Spartan/NFT/blob/main/LICENSE).
