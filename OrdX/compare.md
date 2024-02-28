Protocol Comparison
=====


| - | ordx | Runes | Atomicals |
| :--: | :----: | :----: | :----: | 
| Value Proposition | Digital Treasures | - | Digital Objects |
| Asset Type | FT | FT | NFT+FT | 
| Data Writing | Envelope writing with isolation witness zone based on ord | Writing to OP_RETURN | Envelope writing with isolation witness zone based on "atom" | 
| Ledger Information | Equivalent to UTXO | Custom-built ledger | Equivalent to UTXO | 
| Coloring Scheme | Incomplete coloring | Not applicable | Complete coloring | 
| Base Unit | One token one sat, permanently bound and immutable | Custom | One token one sat, but not bound | 
| Transfer | Direct transfer without writing any data | Direct transfer, but requires writing ledger data in OP_RETURN | Direct transfer without writing any data | 
| Splitting Scheme | Flexible splitting using UTXO model | Infinitely divisible | Scheme undecided (latest news is splitting on AVM) | 
| Burn Possibility | Cannot be burned (sats cannot be burned) | Optional | Possibility of token being burned due to using the wrong wallet or using it incorrectly | 
| Virtual Machine | Not mentioned | Not mentioned | AVM | 
| Layer 2 Network | Lightning Network | Not mentioned | Not mentioned | 

(Runes has not been officially released, and this table will be updated in the future)