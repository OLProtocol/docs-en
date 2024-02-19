如何判断一个Ordinals NFT是ordx资产
====


每一个ordx铸造的结果都是标准的Ordinals NFT，可以按照Ordinals NFT的方式进行转移。    

但是，因为ordx资产铸造的特殊性，在场外进行ordx资产交易的时候，需要对该NFT进行识别，识别所需的所有数据都来Ordinals官方网站（Ordinals.com）或者unisat钱包。如何识别一个NFT是否是有效的ordx资产，我们拿一个 #Pearl 来说明。

1. 获取该nft的铭文序号（#59808557），或者铭文ID（3df5e300dc0b8c67af5dfffb33db0519702138e3728ff6a3a0b6b45426b986bci0） https://ordinals.com/inscription/3df5e300dc0b8c67af5dfffb33db0519702138e3728ff6a3a0b6b45426b986bci0
2. 在ordinals网站查询可见内容，{"p":"ordx","op":"mint","tick":"Pearl","amt":"10000"}
3. 这里需要重点关注，协议是ordx，op是mint，tick是Pearl，amt是10000，同时，我们需要熟悉Pearl的deploy的内容：{"p":"ordx","op":"deploy","tick":"Pearl","block":"828200-828800","lim":"10000","des":"The Oriental Pearl."}（不熟悉的话在ordx.space查看，或者查看这个链接：https://ordinals.com/inscription/4e37618704dbba19f9c26e4eaf99be03bd66e41909f9906d66e886993e32289fi0），Pearl要求在区间828200-828800区间铸造，每次铸造最多10000个币，这是重点检查内容。
4. 回到这个nft的信息，我们可以看到output value是10000，这没问题；查看genesis height是828809，超出deploy所要求的区间了，所以这是一个无效的ordx资产。


另外一种在unisat钱包做判断的方法：
ordx资产在unisat中被识别为一个Ordinals NFT，选择该NFT，关注下内容和占用的sats，然后滚动到最后，点击genesis transaction，跳到mempool查看该NFT的铸造高度，如果在要求范围内，就是有效的ordx资产。  


官网会提供根据铭文序号查询是否是ordx资产的功能。