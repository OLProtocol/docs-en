How to Determine if an Ordinals NFT is an ordx Asset
====

Every result minted by ordx is a standard Ordinals NFT and can be transferred as any other Ordinals NFT .

However, due to the unique nature of ordx assets, when conducting off-chain transactions involving ordx assets, it is necessary to verify the authenticity of the NFT. All the required data for verification can be found on the Ordinals official website (Ordinals.com) or the unisat wallet. Let's use an example of a #Pearl NFT to illustrate how to identify if an NFT is a valid ordx asset.

1. Obtain the inscription number (#59808557) or the inscription ID (3df5e300dc0b8c67af5dfffb33db0519702138e3728ff6a3a0b6b45426b986bci0) of the NFT from https://ordinals.com/inscription/3df5e300dc0b8c67af5dfffb33db0519702138e3728ff6a3a0b6b45426b986bci0.
2. Search for the visible content on the Ordinals website, which should be {"p":"ordx","op":"mint","tick":"Pearl","amt":"10000"}.
3. Pay close attention to the following details: the protocol is ordx, the operation is mint, the ticker is Pearl, and the amount is 10000. Additionally, it is important to be familiar with the deployment details of Pearl: {"p":"ordx","op":"deploy","tick":"Pearl","block":"828200-828800","lim":"10000","des":"The Oriental Pearl."} (If not familiar, refer to ordx.space or this link: https://ordinals.com/inscription/4e37618704dbba19f9c26e4eaf99be03bd66e41909f9906d66e886993e32289fi0). Pearl requires minting within the range of 828200-828800, with a maximum of 10000 coins minted per batch. This is a crucial checkpoint.
4. Looking back at the information of the NFT, we can see that the output value is 10000, which is correct. However, the genesis height is 828809, which exceeds the required range specified in the deployment details. Therefore, this is an invalid ordx asset.  

Another method to determine the validity of an ordx asset is through the unisat wallet:
Ordinals NFTs recognized as ordx assets in the unisat wallet can be selected, and their content and occupied sats should be examined. Scroll to the end and click on the genesis transaction to view the minting height in the mempool. If it falls within the required range, then it is a valid ordx asset.

The official website will provide a functionality to query whether an NFT is an ordx asset based on its inscription number.
