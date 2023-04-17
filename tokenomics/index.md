---
icon: graph
order: 99
---
# VERTO Tokenomics

* **Ticker:** VERTO
* **Contract Address:** Rebuschain (ERC20) [`0x088D38759c2D67eD0DA54d52AEf8d5Fb748Ef70E`](https://evm.rebuschain.com/address/0x088D38759c2D67eD0DA54d52AEf8d5Fb748Ef70E)

## The basics

VERTO is the token that powers the VertoTrade ecosystem.

Earn VERTO from Farms and Pools, or [buy it on the exchange](../../products/exchange/), then explore its use cases:

* A percentage of Verto emissions will be distributed to REBUS stakers in the REBUS-VERTO Minting Pool.
* Stake it in [Minting Pools](../../products/minting-pools/) to earn free tokens
* Use it in [Yield Farms](../../products/yield-farming) to earn more VERTO

But that's not all -- there's much more on the horizon for VERTO!

## Hard CAP
Yes, VERTO has a hard cap of 600M tokens of which ~54% will be burned so there will be a final supply of ~276M VERTO after the first year and 12 years of emission.

## First year (VERTO LAUNCH)
During the first year the token allocation will be slightly different to support the launch of the project and the token:

1. 9M VERTO will be allocated to Treasury.
2. 6M VERTO will be allocated to the Rebuschain Investors via a minting pool that will mint VERTO over a period of nine months.
3. \*Up to 18M VERTO will be allocated to Vertotrade investors via a minting pool that will mint VERTO over a period of nine months.
4. \*3M VERTO will be allocated to the community that will burn 99% of their rebus in a minting pool that will mint VERTO over a period of nine months.

\* Any amount that will not be allocated in these minting pools will be used as farming incentive in liquidity pools for the first year. Final number will be updated once the minting pools are launched.

## Emission rate

Below is the emission rate of VERTO during twelve years after the first launch year. All numbers are approximate based on the average blocktime of 3 seconds of Rebuschain.

### Per block

| **Metric**             | **Emission/block (VERTO)** | **Emission/day (VERTO)** |
| ---------------------- | -------------------------: | -----------------------: |
| Emission               |                        4.2 |                  123,287 |
| Burned Weekly          |                     \~2.16 |                 \~65,753 |
| **Effective Emission** |               **\~2.04\*** |           **\~57,534\*** |

## Other Deflationary Mechanics

{% hint style="info" %}
The burning process is currently manual. [View burn VERTO here](tbd).
{% endhint %}

## Why is the VERTO burn manual?

To hit the ground running, VertoTrade launched with the VertoMintingPool contract emitting 2.04 VERTO per block. When users will perform any operation in VertoTrade VERTO will be minted based on the number of operations and will be moved to the burn smart contract address, which for now will be triggered manually. The goal is for this process to evenutally be automatic.

## How to Confirm VERTO Supply for yourself

To confirm that the circulating VERTO supply shown on the VertoTrade homepage is correct:

1. Head to the VERTO token contract on Rebuschain EVM Explorer and [see how much VERTO is held by the Burn Address.](tbd) That's the total amount of VERTO that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that [Rebuschain EVM Explorer](https://evm.rebuschain.com) shows.
3. This gives you the actual VERTO supply.