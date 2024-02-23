Client Verification
====

It is not practical to rely solely on an indexer for verification, considering factors such as efficiency and cost. Our goal is to enable clients to independently verify assets based on the data from the mainnet, with the indexer serving as a means of efficient data access support. Additionally, the Ordinals protocol itself requires an indexer service to track sats. The ordx protocol needs to know which tickers have been deployed in which blocks and which mints have been successful. However, data beyond this is not necessary.

The deploy and mint commands of the ordx protocol are specifically designed to achieve this goal.

Now let's take a look at how clients can verifiy assets:
For example, suppose a wallet claims to own an asset under the ordx protocol, named A, with a quantity of n. To verifiy that the wallet indeed owns this asset, it only needs to locate which utxo and sat inscribe that asset, and then trace back to the inscription at the time of minting. If found, the client can check if this mint satisfies the rules of A. This entire process only requires the support of the Ordinals protocol service, enabling the client to independently verifiy the asset's validity. The ordx protocol can also provide efficient query services, allowing wallets to directly query whether the SatRange of the utxo falls within the valid SatRange of minting for A. Clients do not need to trust the data provided by us because they can easily verify the data we provide through ordinals.com.