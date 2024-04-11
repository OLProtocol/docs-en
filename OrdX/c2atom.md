Comparison with the Atomicals Protocol
====

On the surface, the ordx protocol and Atomicals protocol appear to be similar. Both protocols issue FT tokens, have a one-token-one-satoshi concept, and are based on UTXO, allowing for direct transfers. However, these similarities are only superficial, as the two protocols are fundamentally different. Let's explore their differences below.

Differences in Concepts
----
The Atomicals protocol is an ambitious and imaginative protocol, with a framework and innovation that are worth learning from. We will continue to follow the development of the Atomicals protocol and draw ideas and technologies that align with our own concepts. Recently, Atomicals published an article introducing its grand vision (https://twitter.com/atomicalsxyz/status/1753879073690956145). In this opportunity, let's also discuss the different concepts of the ordx protocol.

Regarding the first task, Atomicals places great emphasis on POW (Proof of Work) and utilizes Bitwork technology to simulate BTC mining. They believe it is a way "To direct one's own real energy utilization in a peaceful and voluntary way." We have been unable to fully understand this novel token distribution model, so we cannot evaluate whether Atomicals' approach is good or not. We leave it to the market to provide the ultimate judgment. For us, one BTC is enough. The BTC ecosystem does not need another coin that competes for expensive computational resources. The coins growing within the BTC ecosystem generally fall into two categories: coins controlled by project teams, who distribute them at their discretion, and fairly distributed coins where fairness is the core requirement. The ordx protocol gives decision-making power to the project teams. They can deploy their contracts in advance, publicly disclose them, and guide users to fair minting within specific height ranges. Users have the opportunity to mint, and they pay the satoshis and fees required for minting, which is fair enough. There is no need for additional competition for computational power.

Regarding the second task, implementing a Turing-complete technical solution on the BTC mainnet, we maintain respect for the pioneers and continue to track their progress. However, we have always had a question that we haven't fully figured out: Is it necessary to implement a Turing-complete virtual machine on the BTC mainnet? Until we have a clear answer to this question, we won't take action. We tend to collaborate with the mainnet and focus on implementing everything on the Lightning Network, which is our future development direction.

Regardless, the BTC ecosystem needs the exploration and practice of various protocols. We are pleased to have the opportunity to participate in the construction of the BTC ecosystem. We remain committed to the path of the ordx protocol and continue to build it, making the ordx protocol the IP/TCP protocol of the internet.

We have also prepared an article introducing [the design concept of ordx](concept.md), which is not as grand but stands out for its simplicity and understandability. It efficiently utilizes existing infrastructure without reinventing the wheel.

Technological Differences
----
The technological differences are the most obvious and significant. In simple terms, ordx is based on the Ordinals protocol, while Atomicals takes a different approach, being an entirely distinct protocol that competes with Ordinals.

1. Data Writing Method and Format   
ordx's data is encapsulated within the "envelope" defined by Ordinals, making it compatible with the Ordinals protocol. The minting result is a standard Ordinals NFT, which can utilize existing infrastructure such as wallets and exchanges that support the Ordinals protocol.
Atomicals employs its own protocol and format within a similar envelope to the Ordinals protocol. The data is written to the segregated witness area, and it also uses the commit and reveal transactions to disclose the contents of the segregated witness.

2. Binding Relationship with Satoshis   
ordx assets are strictly bound to satoshis, thanks to the numbering of satoshis by the Ordinals protocol. When minting ordx assets, they are bound to a specific satoshi, and this binding is permanent regardless of the location of the satoshi. Each satoshi in the ordx protocol is unique and identifiable due to their numbering.
The Atomicals protocol uses the UTXO model to track and transfer arc20 assets but does not fix them to a specific satoshi. Since the Atomicals protocol does not support the Ordinals protocol, it cannot identify specific satoshis, treating satoshis as fungible within the Atomicals protocol.

3. Coloring Scheme   
ordx does not have a coloring problem because it identifies each satoshi, and whether a satoshi is bound to an asset is determined by its historical data, independent of the satoshi's location.
Atomicals currently only supports a complete coloring scheme, meaning that all satoshis within a UTXO must be colored. Otherwise, it would result in burning.
(Atomicals finally chose the semi-colored solution to solve the splitting problem in 2024.04. This is a contribution of the ordx protocol to the BTC ecosystem.)

4. Splitting Scheme   
Due to its identification and tracking of each satoshi, the ordx protocol can flexibly utilize the UTXO model to split assets, allowing formore granular control and efficient asset management.
Atomicals finally chose a semi-colored solution to solve the splitting problem in 2024.04.

5. Virtual Machine Solution  
The ordx protocol is a relatively new protocol that started its design in November 2023, taking inspiration from Ordinals, BRC-20, and Atomicals. Due to factors such as manpower and time constraints, progress has been slow, and we currently do not have a well-defined virtual machine technology solution. However, we do not believe that the Bitcoin mainnet requires a virtual machine, so this work has been delayed, and we haven't put much thought and planning into it.
Atomicals' AVM has announced a solution where data and logic are placed in one layer and executed in the indexer. This solution does not completely solve the trust and security issues.

6. Layer 2 Network Solution  
Since its inception, the ordx protocol has been focused on the Lightning Network. We have always emphasized that we only develop native BTC technologies. In our view, the Lightning Network is the native layer 2 network supported by BTC. Only such a layer 2 network can ensure the security of user assets and ensure that assets are under the control of users rather than project teams.
The AVM solution of the Atomicals protocol should be their second-layer solution.

7. DID (Decentralized Identifiers)  
The ordx protocol has its own DID solution, which is partially revealed through the restrictions on tick names. The tick length in ordx is a maximum of 16 bytes. We won't disclose the specific details at the moment, but it is completely different from the DID solution in the Atomicals protocol.


Summary
----
The ordx protocol and the Atomicals protocol differ significantly, but both are builders of the BTC ecosystem and aspire to its prosperity. 