
Splitting Solution
====

For ordx assets, splitting is not a fundamental issue as it is natively supported by the BTC UTXO model. Even though the current network imposes limitations on the minimum amount of satoshis in a UTXO due to hardware and network constraints, it is still possible to split ordx assets into a UTXO containing only one satoshi by constructing transactions flexibly. Let's use #Pearl as an example to illustrate the process.

Step 1: Splitting a Pearl asset with 10,000 satoshis into 10 parts using tools like Sparrow (assuming no transaction fees).  
![Initial Split](../assets/substract1.jpg)  
At this point, it can already meet the needs of most cases. By splitting one Pearl into ten, even if the original Pearl increases to 10,000 satoshis, the ten split parts can still be used for a long time. If further splitting is desired, continue to step 2.

Step 2: Flexibly utilize the UTXO model to split the Pearl asset into 1 satoshi.  
![Further Split](../assets/substract2.jpg)  
With the above model, you can split the asset in any way you want if you don't find 1 Pearl too low in value. However, we do not recommend proceeding with step 2. On one hand, the current price of one Pearl is very low, so there is no need to split it further. On the other hand, it would lead to asset fragmentation. Once the second-layer network supported by the ordx protocol is established, we recommend not splitting and directly conducting transactions on the second layer.

Step 3: Split directly on the second-layer network. The second-layer network allows for unlimited splitting without the limitation of one satoshi per unit. However, when transferring back to the mainnet, it must be done in satoshis. Additionally, if there is a sufficient amount of ordx assets, they can be converted back into Ordinals NFTs on the base layer.Please note that the splitting solution provided here is subject to the current limitations and recommendations. As the ordx protocol evolves, new features and optimizations may become available, and it is important to stay updated with the latest developments and guidelines.