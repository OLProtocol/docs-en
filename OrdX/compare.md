Protocol Comparison
=====


| - | OrdX | BRC-20 | Atomicals |
| :--: | :----: | :----: | :----: | 
| Value Proposition | Digital Treasures | - | Digital Objects |
| Asset Type | FT | FT | NFT+FT | 
| Minting Method | Envelope-based writing in isolated witness area based on ord | Envelope-based writing in isolated witness area based on ord | Envelope-based commitment & disclosure using "atom" | 
| Indexing | Relies on ordx indexer | Relies on BRC-20 indexer | Relies on electrumx indexer | 
| Verification | Verified through ordx indexer, client-side verification possible | Verified through BRC-20 indexer, client-side verification not possible | Verified through electrumx indexer, theoretically possible for client-side verification |
| Transfer | Direct transfer | Insrcibe first, then transfer | Direct transfer | 
| Base Unit | One sat represents one unit of the asset, asset is bound to sats and cannot be changed | Bound to addresses | Expected to be one token per sat, but can be adjusted based on the EXP parameter | 
| Splitting Solution | Can be split, utilizing UTXO rules to divide an asset with only 546 sats into arbitrary parts, can be repeated | Infinitely divisible | not yet been finalized | 
| Possibility of Burning | Sats cannot be burned, thus assets cannot be burned | Cannot be burned | Possibility of token being burned due to using the wrong wallet or incorrect usage |