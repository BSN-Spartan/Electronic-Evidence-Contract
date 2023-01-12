## Introduction to Electronic Evidence

Electronic Evidence is a means used to preserve evidence, and there are many application scenarios. For example, in the copyright field, an author can save the signature of his/her work to an evidence service, and when a copyright dispute arises, the dispute can be resolved through forensics. The key part of evidence and forensics is the electronic evidence service. How to ensures its trustworthiness? Will the depository itself damage the evidence data? The traditional centralized depository is difficult to solve this problem. In blockchain technology, a ledger is jointly maintained by various nodes, and its content is determined by the consensus algorithm, so that a single node cannot tamper with the ledger that has reached consensus. This tamper-proof feature is the core of the decentralized electronic evidence solution. In this example, the evidence data is no longer stored in a single institution, but is distributed and stored on all blockchain nodes.


## Business Overview

Electronic evidence is a way to record the whole process of "user identity verification - data creation - data storage - data transmission", and apply a series of security technologies to ensure the authenticity, integrity and security of data in all aspects, which has complete legal effect in justice.

The use of blockchain + smart contract for evidence has the following advantages:
* Tamper-proof mechanism: the use of blockchain technology will preserve evidence data and strengthen the tamper-proof nature of evidence.
* Recognition of the validity of evidence: judicial institutions, as nodes on the chain, are involved in recognizing and signing the evidence data, and the validity of the data can be confirmed by the blockchain.
* Continuous validity of service: After the data is submitted to the chain, it will be permanently preserved and valid even if some validation nodes withdraw from the blockchain.




## Business Process

Create an evidence -> Store the evidence -> Verify the evidence:
* Depositor: submit the evidence to the chain. The blockchain can use digital certificates, time stamps and other technologies to store the system data generated in business processes, agreements, documents and bills signed online, and data that records the operation of all parties, and then generates a unique hash value.
* Depository: save the evidence. In this example, the smart contract on the blockchain acts as the depository.
* Verifier: extract the evidence. When an evidence is submitted to the chain, the verifier can verify the owner, timestamp and other related information of that evidence at any time.



## Interfaces

Submit the evidence：

    - setData(bytes32 hash, address owner, bytes memory remaks, uint timestamp): the depositor submits an evidence to the chain. "hash" is the digest of the evidence, "owner" is the owner of the evidence, "remark" is the description of the evidence, "timestamp" is the time of submission.
        
Verify the evidence：
    
    - getData(bytes32 hash) public view returns(bytes32, address, bytes memory, uint)：the verifier gets the evidence. 

## Example

If you want to create an evidence contract, and submit and check an evidence, the process is as follows:

* Deploy the evidence contract
* The depositor calls Evidence.setData method to submit an evidence
* The verifier calls Evidence.getData to get evidence