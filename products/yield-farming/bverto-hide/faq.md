# FAQ

![](../../../public/assets/how-bVERTO-FAQ.png)

### How are the bVERTO multipliers calculated?

You may notice that you get different bVERTO boost multipliers when staking in different farms.

That's because bVERTO - Farm Boosters multipliers are calculated using the following metrics upon activation or refresh:

* `userLpStakedAmount` : The number of LP tokens you are staking in the farm
* `totalLpStakedAmount` : The total number of LP tokens in the farm
* `userLockedAmount` : The number of VERTO you are staking in the fixed-term staking VERTO pool
* `userLockedDuration` : The staking duration of your fixed-term staking position
* `totalLockedAmount` : The total number of locked VERTO in the fixed-term staking VERTO pool
* `averageLockedDuration` : The average staking duration of the fixed-term staking VERTO pool

The multiplier is calculated using the following method:

1. `resultA = constantA * userLpStakedAmount`
2. `resultB = (totalLpStakedAmount * userLockedAmount * userLockedDuration / constantB) / (totalLockedAmount * averageLockedDuration)`
3. `boostMultiplier = min(userLpStakedAmount, (resultA + resultB)) / resultA`

`constantA` and `constantB` are set by the kitchen and subject to future adjustments based on community feedback and market condition.

Here are some examples of the calculation:

![](../../../public/assets/bVERTO-params.png)

![](../../../public/assets/bVERTO-cal.png)

{% hint style="info" %}
**TL;DR**

The more LP you want to boost

The more VERTO you need to lock for longer durations
{% endhint %}

### Why do my multipliers change even after activation?

Please note that any user actions to the farms or VERTO staking pool will automatically update your boost multiplier based on the latest data and statistics from farms and the VERTO staking pool, including but not limited to:

* Stake/Unstake LP tokens to/from Farm
* Harvest VERTO rewards from Farm
* Extend your VERTO staking duration
* Add more VERTO into your fixed-term staking position
* Convert your VERTO staking position to flexible

{% hint style="warning" %}
Please note:&#x20;

In order to ensure fairness and prevent potential abuse and cheating using out-of-date data. Farm booster is designed to be community governance. Therefore, anyone can call `refresh(address _user, uint256 _pid)` function on the farm booster contract (link) to refresh anyone's boost multipliers using the latest data.
{% endhint %}

### Where are my VERTO rewards after activating or unsetting the booster?

![](../../../public/assets/bVERTO-has-pending-balance.png)

While farming with bVERTO - Farm Boosters, some of your harvested VERTO rewards may be temporally stored in the farm booster contract. Whenever this happens, you will see a dotted line under your "VERTO EARNED", indicating that apart from the number shown, you have more VERTO rewards in the farm booster contract.

**This part of the VERTO rewards will be automatically sent to your wallet upon the next harvest, deposit or withdrawal.**

To harvest them right now, simply click the "Harvest" button.

![](../../../public/assets/bVERTO-has-pending-balance-tooltip.png)

To check the number of extra rewards in the farm booster contract, hover or long-press the number with the dotted line.

### Why I'm not able to boost a farm

1. Farm booster is only available for selected farms. More farms will be made available in the future. For now, look for the "Boosted" tag on the UI.\
   ![](<../../../public/assets/bVERTO-boost-tag (1).png>)
2. There is a limit to the number of farms that are able to boost simultaneously. To check the number of remaining boosters, refer to the panel on top. \
   ![](<../../../public/assets/bVERTO-farm-number-limit (1).png>)\
   You will need to unset an active booster in order to activate boosters on other farms.
3. Make sure you've completed the one-time setup.
4. Due to the involvement of multiple contracts, some of the contract interactions require slightly more gas tokens (BNB). So please make sure you have enough BNB in your wallet.

### What is the maximum bVERTO Boost Multiplier I can get?

Currently, the maximum boost a user can get for a farm booster is 2x. Which offers them double the baseline APRs.

### How can I increase my bVERTO Boost Multipliers?

* Add more VERTO into the fixed-term staking position
* Extend the duration of your fixed-term staking position

Simply put:

> Stake more VERTO, stake for longer

[Learn more about how the bVERTO boost multipliers are calculated](faq.md#how-are-the-bcake-multipliers-calculated).

### Where are the extra boosted VERTO rewards coming from?

**Relax, no extra emissions are allocated in order to make bVERTO possible.**

Similar to fixed-term VERTO staking. bVERTO boosts individual users' share against the others.

Even though the baseline APR may drop after the deployment of bVERTO. Mercators believe it is a good tradeoff as it not only benefits loyal VERTO lovers by boosting their farming yield, but also creates more demand for VERTO and serves as a great incentive for VERTO staking.

### Why the gas usage is high when enabling farm booster for the first time?

To enable bVERTO - farm booster, users must set up a proxy wallet address, which requires deploying a new contract. This process is relatively gas heavy. (around $2\~5 based on the BNB price and the condition of the blockchain)

However, the setup process is one-time-only for each wallet address. You only need to perform it once.

### Why the multiplier I receive is low?&#x20;

bVERTO - farm booster works in a way by evaluating both your fixed-term VERTO staking position and your liquidity farming position. Simply put:

> If users want to boost more LP tokens in farm, they will need to lock more VERTO for longer durations in pool.

This design ensures the benefits are not only offered to large holders, but to any user who has a sizable VERTO staking position when compared to the farming position.&#x20;

Learn more about how the multiplier is calculated [here](faq.md#how-are-the-bcake-multipliers-calculated).

### Why only VERTO/BUSD? Why only 1 farm?

Since bVERTO involves updating one of VertoTrade's core products, which is liquidity farming. Mercators want to take a slower and more steady approach to the launch.&#x20;

Therefore, in the initial product release phase. Many of the parameters are very conservative. Including the number of farms users can boost, which farm users can boost, as well as the difficulty parameter in receiving the boost multiplier.

After the initial release phase, Mercators will adjust the parameters based on the community feedback.

### Is bVERTO audited?

bVERTO has been audited by both internal and external auditors.&#x20;

Check out PeckSheild's audit report [here](https://github.com/peckshield/publications/tree/master/audit\_reports/PeckShield-Audit-Report-VertoTrade-FarmBooster-v1.0.pdf).

