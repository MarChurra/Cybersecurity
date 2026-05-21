## BlockChain
- A distributed ledger
  - Keep track of transactions
- Everyone on the blockchain network maintains the ledger
  - Records and replicates to anyone and everyone
- Many pratical applications
  - Payment processing
  - Digital iidentification
  - Supply chain monitoring
  - Digital Voting

## The Blockchain process
- A transaction is requested
- The transaction could be any digital transaction from transferring Bitcoins, medical records, data backups, or transferring house title information
1. The transaction is sent to every computer (node) in a decentralized network to be verified.
2. The verified transaction is added to a new block of data containing other recently verified transactions
3. A secure code (hash) is calculated from the previous blocks of transaction data in the blockchain.
4. The hash is added to the new block of verified transactions.
5. The block is added to the end of the blockchain, which is then updated to all nodes in the network for security
6. The transaction is complete.
- If any blocks are altered, its hash and all following hashes in the chain are automatically recalculated.
- The altered chain will not longer match the chains stored by the rest of the network, and will be rejected
