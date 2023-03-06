# FAQ

<figure><img src="../../../public/assets/image (4).png" alt=""><figcaption><p>\</p></figcaption></figure>

### What should I do on VertoTrade on other blockchains?

Provide liquidity, trade and farm as you always have been. If you are a multichain user already, remember to provide liquidity on VertoTrade on other blockchains that we've deployed on (like Ethereum), as we have VERTO rewards on Rebuschain for you, allowing you to earn even more VERTO without bridging those assets over!

### **Will there be more pairs?**

Yes, but we will be deploying in steps to ensure we prioritize the safety of user funds and VERTO inflation. Do let us know in the community chats what you think should be added to VertoTrade on other blockchains, as well as what other blockchains we should deploy VertoTrade on.

### **Why the gas cost for staking LP tokens is high?**

A small amount of native token (for example, ETH on Ethereum) is required for the first-time setup. So the first transaction will be slightly costly.

Plus, there are other fees (mostly gas costs) involved in cross-chain farming. Check out [this](faq.md#are-there-any-fees-when-i-do-crosschain-farming) dedicated section to learn more.

### **Why do staking and unstaking take 30 minutes to complete?**

All cross-chain transactions will take around 30 minutes to complete. It is because:

* Transactions have to be executed on both the farming blockchain (like Ethereum) and the REBUS Chain.
* Delivering cross-chain messages takes time.
* To ensure safety and all the data are synced and consistent between different blockchains.

### **Where are my harvested VERTO rewards?**

Your harvested VERTO will be distributed on Rebuschain. Please switch the blockchain network in your wallet to check the balance of VERTO.

### **I can't harvest because my wallet doesn't support switching between different blockchains!**

Please try using a different wallet app that supports multichain and chain switching.

Please note that staking and unstaking LP tokens will also harvest all the earned VERTO to your wallet on Rebuschain. Therefore if you don't want to use a different wallet app, simply stake more, or unstake a tiny amount of LP tokens to harvest your earned VERTO.

### Are there any fees when I do crosschain farming?

Unlike farming natively on REBUS Chain, farming on other blockchains requires cross-chain activities. Here are the fees involved:

**1 - Gas fee to create a proxy contract**

A proxy contract has to be created on the REBUS Chain for cross-chain farming. The gas cost for proxy contract creation is included in the transaction.

This fee only charges once upon the first "stake" transaction.

**2 - Gas fee for calls on REBUS Chain**

When users deposit or withdraw LP tokens. An executor will perform transactions calling on behave of the users on the REBUS Chain. The gas cost for these calls is included in the transaction.

This fee is charged in every deposit or withdrawal transaction.

**3 - Gas fee for calls on other blockchains**

When users withdraw LP tokens. An executor will perform the final transactions calling to release the LP tokens on other blockchains (like Ethereum). The gas cost for these calls is included in the transaction.

This fee is only charged in withdrawal transactions.

**4 - Cross-chain messaging fee**

We utilise a message bus powered by Celer to route our cross-chain messages. Therefore a messages fee is included based on the byte length of the message.

This fee is charged in every stake transaction. In unstake transactions, this fee is charged twice since a two-way communication between REBUS Chain and other blockchains is required for safety.

```
messagingFee = feeBase + message.length * feePerByte;
```

You may find the variables in the formula with in the message bus contract:

* Ethereum: `0x4066d196a423b2b3b8b054f4f40efb47a74e200c`
* REBUS Chain: `0x95714818fdd7a5454f73da9c777b3ee6ebaeea6b`

**5 - The starter fund**

This is not strictly a "fee".&#x20;

For every new user who started doing VertoTrade cross-chain farming. In the first “stake” transaction, we will deposit 0.005 REBUS into their REBUS Chain wallet. The corresponding amount of native tokens on the farming chain (like ETH on Ethereum) will be charged from the deposit transaction, using the market rate provided by the price oracle.

This is to help users start their REBUS Chain journey with ease. We understand the painfulness of having all the harvested VERTO but not being able to explore the vivid VertoTrade ecosystem without finding another way to acquire REBUS for gas.

This fee only charges once upon the first "stake" transaction.

### Where are the emissions coming from?&#x20;

_updated on Oct 10 2022_

For now, Mercators have diverted 0.0189 VERTO per block from the VERTO pool to all crosschain farms.&#x20;

Here is the emissions breakdown:

|                          | Multiplier | VERTO per block |
| ------------------------ | ---------- | -------------- |
| **VERTO Pool**            | -          | **8.9811**     |
| **All Crosschain Farms** | -          | **0.0189**     |
| Ethereum ETH/USDC        | 0.5x       | 0.0105         |
| Ethereum ETH/USDT        | 0.2x       | 0.0042         |
| Ethereum WBTC/ETH        | 0.2x       | 0.0042         |

### What happened during the deposit, harvest and withdrawal?

VertoTrade crosschain farming is like using a "stand-in" LP token to farm on the REBUS Chain, with the same VertoTrade OptimusMercator. The VERTO rewards are calculated and distributed on REBUS Chain, controlled and guarded by the same OptimusMercator contract.

#### Upon Deposit:

1. Users request depositing LP tokens on farming blockchains (like Ethereum).
2. LP tokens are being transferred to farming vault contracts.
3. Celer message bus is utilised to deliver the "deposit" message to REBUS Chain.
4. An executor on REBUS Chain mints the same amount of farming tokens as "stand-ins", and then deposits them into the farms.

#### Upon Harvesting:

Since VERTO rewards are calculated and distributed on REBUS Chain. Users can claim their VERTO rewards with a single REBUS Chain transaction without the need for cross-chain operations.

#### Upon Withdrawal:

1. Users request withdrawing LP tokens on farming blockchains (like Ethereum).
2. Celer message bus is utilised to deliver the "withdraw" message to REBUS Chain.
3. An executor on REBUS Chain withdraws the farming tokens from the farms, burns those tokens, transfers the earned VERTO to users, and utilises the Celer message bus to deliver the confirmation message back to the original farming blockchain.
4. An executor on the farming blockchain confirms everything and then releases the LP tokens from the vault contracts.
