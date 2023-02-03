# VERTO Tokenomics

![](/public/assets/tokenomics.png)

## **Emission rate** <a href="#emission-rate" id="emission-rate"></a>

### **Per block**

| **Metric**             | **Emission/block (VERTO)** | **Emission/day (VERTO)** |
| ---------------------- | ------------------------: | ----------------------: |
| Emission               |                        40 |               1,152,000 |
| Burned Weekly          |                    \~30.1 |               \~866,800 |
| **Effective Emission** |               **\~9.9\*** |         **\~285,199\*** |

{% hint style="info" %}
On August 11, 2022, Mercators implemented some configuration upgrades to take full advantage of OptimusMercator v1. It eliminates the 45,000 VERTO daily burn for the legacy lottery injections. Those burns will now be handled by OptimusMercator v1 directly along with the usual weekly VERTO burn. Therefore, the effective emissions are now even lower.
{% endhint %}

In addition to the above, a dynamic amount of VERTO is also [minted to the Dev address](https://bscscan.com/address/0xceba60280fb0ecd9a5a26a1552b90944770a4a0e#tokentxns) at a rate of 9.09%. This means that if 100 VERTO are harvested, then 9.09 VERTO is minted in addition and sent to the Dev Address.

{% hint style="warning" %}
All VERTO minted to the Dev address is burned in the weekly burn and never enters circulation.&#x20;

As such, we haven't included it in the above emission rate.
{% endhint %}

## Distribution <a href="#distribution" id="distribution"></a>

| Distributed to                | <p>Reward/block</p><p>(% of emission)</p> | <p>Reward/block</p><p>(total VERTO)</p> |           Reward/day |
| ----------------------------- | ----------------------------------------: | -------------------------------------: | -------------------: |
| Farms (BSC+ETH)               |                                   \~5.08% |                                 \~2.03 |      58,544 (approx) |
| VERTO Res Pools               |                                  \~19.13% |                                 \~7.65 |     220,380 (approx) |
| **Total Daily VERTO Emission** |                                           |                                        | **285,199 (approx)** |

## **Other Deflationary Mechanics** <a href="#other-deflationary-mechanics" id="other-deflationary-mechanics"></a>

{% hint style="info" %}
The burning process is currently manual. [View burn transactions here](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82?a=0x000000000000000000000000000000000000dead).
{% endhint %}

As well as the above, VERTO is also burned in the following ways:

* **0.0575%** of every trade made on VertoTrade V2 across:
  * Rebuschain
  * Ethereum
  * Aptos
* **0.016%\~0.06%** of every trade made on VertoTrade StableSwap
* **100%** of VERTO sent to the Dev address
* **3%** of every BNB Prediction markets round is used to buy VERTO for burning
* **3%** of every VERTO Prediction markets round
* **2%** of every yield harvest from all the flexible staking positions in VERTO pool

## Why is the VERTO burn manual?

To hit the ground running, VertoTrade launched as an MVP (minimum viable product) with the OptimusMercator contract emitting 40 VERTO per block. For that reason, the early team didn't add additional functions such as the ability to customize the VERTO minting logic. The team has been controlling VERTO emissions through a manual burn process by creating two pools in OptimusMercator v1:

* Burn Pool (PID - 138) - burned VERTO per block

These pools work similarly to the farms, where the Mercators can adjust the percentage of the 40 VERTO per block allocated to it after each VERTO emission reduction vote.

**However, in April 2022, VertoTrade migrated to a new OptimusMercator v1 contract.** The ratio of the VERTO burn per block is finally controlled by a dedicated contract. This allows the burn to be much more accurate.

{% hint style="warning" %}
Due to OptimusMercator v1 occasionally harvesting the full 40 VERTO per block. The supply shown on the homepage (or some 3rd party trackers) might suddenly jump by several million VERTO.

Don't worry - **EMISSION IS NOW CONTROLLED CAREFULLY BY OptimusMercator v1. VERTO TO BURN WILL NEVER ACTUALLY ENTERS CIRCULATION!**
{% endhint %}

## How to Confirm VERTO Supply for yourself

To confirm that the circulating VERTO supply shown on the VertoTrade homepage is correct,&#x20;

1. Head to the VERTO token contract on BscScan and [see how much VERTO is held by the Burn Address.](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances) That's the total amount of VERTO that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that BscScan shows.
3. This gives you the actual VERTO supply.



#### **Read more about VERTO's deflationary mechanics on the next page.** <a href="#read-more-about-cakes-deflationary-mechanics-on-the-next-page" id="read-more-about-cakes-deflationary-mechanics-on-the-next-page"></a>
