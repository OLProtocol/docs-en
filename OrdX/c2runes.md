Comparison with the Runes Protocol
====

During the holiday break, we thoroughly studied Casey's blog (https://rodarmor.com/blog/runes/) and an article he recommended introducing the Runes protocol (https://github.com/zhiqiangxu/btc_notes/blob/main/ordinal_runes.md). Only then did we have a complete understanding of the Runes protocol. Based on the information we have gathered so far, it appears that the Runes protocol has little to do with the Ordinals protocol. This came as a surprise to us. With the Ordinals protocol deeply ingrained and having a significant market impact with a large user base, Casey decided to completely abandon the Ordinals protocol and adopt new technologies, terminology, and naming conventions in the Runes protocol. This not only confuses users and increases their learning curve but also adds development costs for the Runes protocol's support in the development community. Both wallets and trading markets must be redesigned to be compatible with both Ordinals' NFTs and Runes' FTs. While we are not Casey and do not know the considerations behind his decision, we are disappointed with the outcome of his new protocol having no connection to the Ordinals protocol. It seems that Casey may have overlooked the enormous potential of the Ordinals protocol, which poses a significant obstacle to its adoption.

Since the Runes protocol has no relation to the Ordinals protocol, and the ordx protocol is based on the Ordinals protocol, the differences between these two protocols are expected to be substantial. Based on the available information, we can provide a brief comparison between the two protocols. A more detailed comparison may be possible once the Runes protocol is launched.  


Compatibility
----
The ordx protocol is based on the Ordinals protocol, taking only a small step forward from its foundation, almost insignificant. However, this small step brings significant benefits as ordx and the Ordinals protocol are mutually compatible at a certain level. Before being split, ordx assets are standard Ordinals NFTs, allowing the ordx protocol to effectively leverage the well-established infrastructure of the Ordinals protocol in the market. This eliminates the need to build wallets, browsers, swap trading markets, and even indexers from scratch. The verification and tracking of ordx assets' validity can be done by wallets with just a few lines of verification code.

In terms of form, the Runes protocol has deviated significantly, having no connection to the Ordinals protocol. This means that the existing infrastructure for Ordinals cannot support the Runes protocol, requiring redevelopment. However, in essence, the Runes protocol is more similar to BRC-20, as both have built a new ledger but haven't fully utilized the concept of satoshis.

Data Writing Method and Format
----
The data in ordx is encapsulated within the "envelopes" defined by the Ordinals protocol, using the widely accepted and recognized JSON format, similar to BRC-20. This data is written in the segregated witness area.

In contrast, the Runes protocol writes data in the OP_RETURN field, which has limited space. Therefore, it adopts a compact data format that cannot be directly viewed.

Relationship with Satoshis
----
ordx assets are strictly bound to satoshis, thanks to the numbering of satoshis in the Ordinals protocol. This binding is permanent, regardless of the location of the satoshis. Each satoshi is unique and identifiable within the ordx protocol due to the numbering of satoshis.

The Runes protocol does not use the Ordinals protocol and does not bind to satoshis.

Transfer
----
The transfer of ordx is similar to the transfer of BTC, without any additional requirements.

Runes, similar to BRC-20, requires a transfer instruction for the transfer to occur. The advantage over BRC-20 is that it does not require engraving before transferring; instead, the transfer instruction is written in the OP_RETURN field during the transfer.

Burning
----
Ordx assets are bound to satoshis and cannot be burned since satoshis cannot be destroyed. If burning is desired, the satoshis can be sent to the genesis address.

The Runes protocol provides a burning option, allowing users to actively choose to burn assets.

Splitting Mechanism
----
Ordx can flexibly utilize the UTXO model and split into a single UTXO containing only one satoshi with the ordx asset. However, satoshis are the smallest unit and cannot be further split.

Runes, similar to BRC-20, uses its own ledger, allowing for flexible splitting. Users can determine the decimal places for splitting.

Learning Curve
----
ordx references the BRC-20 protocol and reuses the token format from BRC-20. The benefit is that users are already familiar with and have accepted the token format of BRC-20, resulting in minimal learning curve, requiring only an understanding of the different parameters involved.

Runes does not have a user-readable protocol format since its data is written in the OP_RETURN field, limited to 80 bytes, and can only use a compact data format. Users cannot directly see the protocol content, which creates a stronger sense of unfamiliarity. Furthermore, the technology for issuance, minting, and transfer in Runes differs significantly from BRC-20. All these differences contribute to a significant learning curve.

Distribution
----
ordx protocol strongly advocates for fair distribution and fully supports the need for fair distribution in its design. However, it does not exclude the possibility of a project fully controlling the distribution. How to use it is entirely determined by the project. The ordx protocol is completely open, and the protocol development team does not control any additional resources in the protocol ecosystem. All resources are open to the community for independent development.

The Runes protocol currently appears to be less open, resembling a project rather than a protocol:
1. The release of ticker names is being slowly controlled, with the names treated as a resource.
2. How will previously issued assets using the Runes protocol be handled? Will they be prevented from upgrading to the official Runes protocol just to compete for being the first? This is a more centralized approach.


Summary
----
Runes does not use the Ordinals protocol, which greatly disappoints us regarding Runes. It seems that only the development team of the ordx protocol recognizes the importance of the Ordinals protocol, placing it in a similar position to the IP/TCP protocol. We will adhere to this conclusion and continue to promote the infrastructure and applications of the Ordinals protocol, ensuring that assets issued based on the Ordinals protocol hold a significant position in the BTC ecosystem.

(To be continued, awaiting updates)
