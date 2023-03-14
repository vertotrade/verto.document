# Yield Farming

Yield Farms allow users to earn VERTO while supporting VertoTrade by staking LP Tokens.

Check out our [How to Use Farms guide](how-to-use-farms.md) to get started with farming.

{% hint style="warning" %}
Yield farming can give better rewards than Pools, but it comes with a risk of **Impermanent Loss**. It’s not as scary as it sounds, but it is worth learning about the concept before you get started.

Check out this great [article about Impermanent Loss ](https://academy.binance.com/en/articles/impermanent-loss-explained)from Binance Academy to learn more.
{% endhint %}

## Reward calculations

Yield Farm APR calculations include both:

* **LP rewards APR** earned through providing liquidity and;
* **Farm base rewards APR** earned staking LP Tokens in the Farm.

Why? Because when you stake your LP tokens in a farm to earn VERTO, you're still providing liquidity to the liquidity pool, so you earn LP rewards as well!
<!--
![Farms APR](/public/assets/farms-apr.png)
-->
So how do we calculate those figures?

### Calculating Farm Base Reward APR

The **Farm Base APR** is calculated according to the farm multiplier and the total amount of liquidity in the farm -- this is the amount of VERTO distributed to the farm.

### Calculating LP Reward APR

On top of that, farmers receive **LP rewards** for providing liquidity. Here's an example of calculating **LP rewards**:

In a sample VERTO/REBUS pair, we have these values:

**Liquidity:** $387.42K\
**Volume 24H:** $96.97K\
**Volume 7D:** 709.73K

* Calculate yearly fees
  * Use the 24H volume to calculate the **fee share** of liquidity providers in the pool (based on the 0.17% trading fee structure):\
    $96,970\*0.17/100 = **$164.849**
  * Next, use that **fee share** to estimate the projected **yearly fees** earned by the pool (based on the current 24h volume):\
    $164.849\*365 = **$60,169.885**
* We can now use the yearly fees to calculate the **LP rewards APR:** That's **yearly fees** divided by **liquidity:**\
  ($60,169.885/$387,420)\*100 = **15.53% LP reward APR**
