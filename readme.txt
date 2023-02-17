zkSync relies on a smart contract deployed to the Ethereum network to hold all assets, while most computations are performed off-chain. Every time you sign a transaction, the protocol submits it to operators who roll up multiple transactions (potentially thousands) into a block, and compute the following:

cryptographic commitment (root hash)
cryptographic proof (the SNARK)
state ∆, representing a small amount of data for each transaction
All this stuff is then sent to the smart contract running on the Ethereum network. This enables an interested party to reconstruct the state at any given point in time.

The SNARK verification is significantly cheaper than verifying every transaction individually, and storing the state off-chain is also much cheaper than storing it in EVM.

This enables a boost in scalability and transaction cost savings.