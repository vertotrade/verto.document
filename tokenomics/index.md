---
icon: graph
order: 99
---
# VERTO Tokenomics

* **Ticker:** VERTO
* **Contract Address:** Rebuschain (ERC20) [`0x0TBD`](https://tbd)

## The basics

VERTO is the token that powers the VertoTrade ecosystem.

Earn VERTO from Farms and Pools, or [buy it on the exchange](../../products/exchange/), then explore its use cases:

* 25% of Verto emissions will be distributed to REBUS stakers in the REBUS-VERTO Minting Pool.
* Stake it in [Minting Pools](../../products/minting-pools/) to earn free tokens
* Use it in [Yield Farms](../../products/yield-farming) to earn more VERTO

But that's not all -- there's much more on the horizon for VERTO!

## Hard CAP
Yes, VERTO has a hard cap of 600M tokens.

## Emission rate

Below is the emission rate of VERTO all numbers are approximate based on the average blocktime of 3 seconds of Rebuschain.

### Per block
<!--
| **Metric**             | **Emission/block (VERTO)** | **Emission/day (VERTO)** |
| ---------------------- | -------------------------: | -----------------------: |
| Emission               |                          9 |                  259,200 |
| Burned Weekly          |                        \~6 |                \~172,800 |
| **Effective Emission** |                  **\~3\*** |           **\~86,400\*** |
-->
| **Metric**             | **Emission/block (VERTO)** | **Emission/day (VERTO)** |
| ---------------------- | -------------------------: | -----------------------: |
| Emission               |                        8.4 |                  249,920 |
| Burned Weekly          |                      \~4.8 |                \~138,240 |
| **Effective Emission** |                **\~3.6\*** |          **\~103,680\*** |

## Distribution

| Distributed to                 | Reward/block<br />(% of emission) | Reward/block<br />(total VERTO) |           Reward/day |
| ------------------------------ | --------------------------------: | ------------------------------: | -------------------: |
| Trading                        |                           \~6.4%  |                          \~0.54 |      15,552 (approx) |
| Farming                        |                          \~10.7%  |                           \~0.9 |      25,920 (approx) |
| VERTO Minting Pools             |                            \~25%  |                           \~2.1 |      60,480 (approx) |
| Other                          |                           \~0.5%  |                          \~0.06 |        1728 (approx) |
| **Total Daily VERTO Emission** |                                   |                                 | **103,680 (approx)** |

## Other Deflationary Mechanics

{% hint style="info" %}
The burning process is currently manual. [View burn transactions here](https://tbd).
{% endhint %}

## Why is the VERTO burn manual?

To hit the ground running, VertoTrade launched with the OptimusMercator contract emitting 8.4 VERTO per block. For that reason, the team didn't add additional functions such as the ability to customize the VERTO minting logic. The team controls VERTO emissions through a manual burn process by creating a pools in OptimusMercator v1:

* Burn Pool (PID - TBD) - burned VERTO per block

These pool work similarly to the farms, where the Mercators can adjust the percentage of the 9 VERTO per block allocated to it after each VERTO emission reduction vote.

## How to Confirm VERTO Supply for yourself

To confirm that the circulating VERTO supply shown on the VertoTrade homepage is correct:

1. Head to the VERTO token contract on Rebuschain EVM Explorer and [see how much VERTO is held by the Burn Address.](https://tbd) That's the total amount of VERTO that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that Rebuschain EVM Explorer shows.
3. This gives you the actual VERTO supply.