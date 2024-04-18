Instructions
====

The ordx protocol references the Atomicals protocol and the BRC-20 protocol. In terms of ideology, it is closer to the Atomicals protocol, while in terms of implementation, it is closer to the BRC-20 protocol.

The ordx protocol only has two instructions: deploy and mint. It does not require a transfer instruction. The basic principle is that each unit of asset is bound to one satoshi, so transferring the satoshi also means transferring the asset. Therefore, there is no need for additional ledger records of asset transfer history, nor is there a need to inscribe transfer instructions before the transfer. 

deploy
----

| KEY | Required | Description |
| :---: | :---: | :------- |
| p	| Yes | Protocol name: ordx |
| op | Yes | Instruction: deploy |
| tick | Yes | Token name: allowed characters are 3 or 5-16 characters long (4 characters reserved for BRC-20) |
| lim | No | The limit of tokens minted at a time. The default is 10,000. If minting tokens on a specific satoshi, the default is 1. |
| selfmint | No | The default is false; set to true, only the address holding the ticker can mint (parent-child inscription) |
| block | No | No total supply limit, but specifies the starting and ending block heights for minting (start-end). (Choose either block height range or satoshi attributes.) |
| attr | No | Requirements for satoshi attributes, for example: "rar=uncommon;trz=8". Can be expanded. |
| des | No | Description content |

For example:  
{  
  "p": "ordx",  
  "op": "deploy",  
  "tick": "satoshi",  
  "block": "830000-833144",  
  "lim": "10000"  
}  

The attr field is an expandable attribute that allows more special satoshis to be filtered out using this attribute. Currently supported attributes are:
1. rar: Rarity defined in Ordinals: common, uncommon, rare, epic, legendary, mythic
2. trz: Trailing zeros, specifies the number of trailing zeros in the satoshi number, for example, trz=8 indicates that the satoshi number has 8 trailing zeros.

If you have any good ideas or discover satoshis with special value, you can submit the code to us.

Through the deploy instruction, we can see that the ordx protocol differs from other protocols mainly in the following aspects:
1. One satoshi is bound to one unit of asset.
2. There is no supply limit; instead, the effective block height for minting is specified. All tokens minted within this height range are valid.
3. Support the project party’s overall control through the parent-child inscription..
4. It is possible to specify that only satoshis with certain attributes can be minted, meaning that assets can only be bound to satoshis with specific attributes.

mint
----

| KEY | Required | Description |
| :---: | :---: | :------- |
| p	| Yes | Protocol name: ordx |
| op | Yes | Instruction: mint |
| tick | Yes | Token name: allowed characters are 3 or 5-16 characters long (4 characters reserved for BRC-20) |
| amt | No | The quantity of tokens to mint. Defaults to the value of "lim" from the deploy instruction. Cannot exceed "lim". |
| sat | No | The serial number of the satoshi. If the ticker has attributes set in the deploy instruction, a satoshi that satisfies the conditions must be provided during minting. |

For example:  
{  
  "p": "ordx",  
  "op": "mint",  
  "tick": "satoshi"  
}  

General checks that need to be performed during each mint:
1. The protocol must be ordx.
2. The op must be mint.
3. The tick must have been deployed.
4. The amt must be less than or equal to the "lim" specified in the deploy instruction.
5. If the "selfmint" rule is specified in the deploy instruction: Only the address holding the ticker can mint (parent-child inscription).
6. If the "block" rule is specified in the deploy instruction: The block height for this mint must be within the specified range.
7. If the "attr" rule is specified in the deploy instruction: The satoshi parameter must be provided during minting, and the satoshi must pass the checks based on the attributes specified in "attr":
   - If the "rar" attribute is present: Check if the satoshi belongs to this rarity.
   - If the "trz" attribute is present: Check if the satoshi's serial number has enough trailing zeros.

If any of the above rules are not met, minting is not allowed. Even if a tool tries to force a mint, ordx's indexer will consider it invalid. Wallets can independently verify each token using the indexer of the Ordinals protocol and the data from the Deploy instruction.

upgrade
----
Upgrades other protocols' FT (fungible tokens) to ordx, primarily supporting BRC-20. More extensions in the future. For example:  

{  
  "p": "ordx",  
  "op": "upgrade",  
  "tick": "ordi",  
  "amt": "1000",  
  "org": "brc-20",  
  "cfactor": "1"  
}  

Possible solution:
Lock the tokens into the Lightning Network channel using the OLD protocol and directly convert them into ordx assets and destroy the old tokens when withdrawing.