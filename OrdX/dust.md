Splitting Issue
====

The dust problem is merely a temporary issue that arises from the current hardware conditions not meeting the ideal requirements for the operation of the BTC network. Setting a dust limit clearly goes against Satoshi Nakamoto's original design, as satoshis are meant to be the smallest unit of Bitcoin.

Let's consider this problem from a different perspective. Suppose the following conditions are met:
1. The value of BTC increases by 100 times, for example, making one BTC worth 100 million dollars.
2. Hardware and network conditions improve by 100 times.

If the above conditions are met, is the dust problem still a problem? At that point, one satoshi would be equivalent to 1 dollar, and transferring a satoshi would become a common requirement. From a developmental perspective, how long would it take to achieve the above hypothetical conditions? We are confident that in the near future, UTXOs will directly support the transfer of one satoshi. Furthermore, the value of one satoshi may increase to a level where it needs to be split into smaller units on the second layer of the BTC network. Based on the above conclusion, we do not intend to solve the current UTXO minimum limit issue on the BTC mainnet.

However, the demand for asset splitting still exists. To address asset splitting under the current conditions, we provide three solutions:
1. Optimal Solution: Solve the splitting issue on the second layer of the BTC network. This is one of our main upcoming tasks, and the new protocol is named the Ordinals Lightning DEX Protocol (OLD protocol). On a DEX that supports the OLD protocol, assets can be split almost infinitely. However, when transferring back to the mainnet, the current minimum UTXO limit still needs to be followed, but only one satoshi can be bound to the asset.
2. Temporary Solution 1: Define assets with careful consideration, ensuring that each asset is bound to a sufficient number of satoshis, such as 10,000 satoshis. This way, the asset can be split into at least 10 UTXOs, each containing 1,000 satoshis.
3. Temporary Solution 2: Flexibly utilize UTXOs. By combining the smallest UTXO that contains a certain asset (546 satoshis) with two other UTXOs, the asset contained in the UTXO can be split into any two smaller parts. By repeating this process, a satisfactory result can be achieved. The downside is that the operation becomes too complex.

![拆分](../assets/substract.jpg)

