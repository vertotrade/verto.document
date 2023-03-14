---
visibility: hidden
---
# VERTO Res Pools FAQ

## FAQ

### What lock duration can we choose?

You can choose from 1-52 weeks. The longer the grater the rewards.

### What variables affect the new VERTO Res Pools yield %s (Flexible and Fixed-Term Staking options)?

Since flexible staking and fixed-term staking options are part of the same pool, the following variables affect the yield% (APR/APY) of both:

* Total VERTO staked in flexible staking and fixed-term staking (the sum of both). The more VERTO staked, the lower the APR/APY.
* Total locked VERTO in fixed-term staking. The more VERTO locked means more yield boosts, resulting in fewer VERTO rewards for others (especially flexible staking).
* The average lock duration of all VERTO locked in fixed-term staking. If the average lock duration increases, APR/APY will decrease.

### Can I harvest the rewards during the locked period?

No. You can harvest the rewards only when the locked duration is ended. This is based on the yield/return we are providing as well as the technical implementations.

### Can I extend the lock duration?

Yes. Extending the lock duration adds more time to your **initial lock duration**. When choosing to extend your lock duration, note:

New extended lock duration = initial lock duration + added duration

### Can I remove my VERTO from Fixed-Term staking via contract if I change my mind?

No. Your VERTO cannot be removed or withdrawn from fixed-term staking at any point in time until your lock duration ends and your VERTO is unlocked.

### What is the "VERTO Locked" amount?

The "VERTO Locked" amount is a user's initial locked VERTO balance plus VERTO rewards to date

VERTO Locked = Initial locked VERTO balance + VERTO rewards

When adding more VERTO to fixed-term staking, the "VERTO to be locked" amount is the user's initial locked VERTO balance, VERTO rewards to date, and the VERTO being added.

### Can the Fixed-Term Staking VERTO pool APR change after I lock my VERTO?

Yes, the fixed-term staking VERTO pool APR is variable, just like the old VERTO pools. The fixed-term staking VERTO pool APR is not fixed and is dependent on:

* Total VERTO staked in the VERTO pool (the sum of both Flexible + Fixed-Term Staking).
* The average lock duration of all VERTO locked in fixed-term staking.
* A yield boost (similar to a multiplier) calculated from a user's initial lock duration. The longer you lock your VERTO, the higher the yield boost.

For example, if you lock your VERTO for 52 weeks, your yield boost will be larger than if you lock your VERTO for 26 weeks. The yield boost increases linearly the longer you lock your VERTO.

### Can I use both the Flexible Staking VERTO pool and the Fixed-Term Staking VERTO pool at the same time?

Yes, when you are doing fixed-term VERTO staking. A flexible VERTO staking side-pool will automatically appear for you to choose from.

### Is there a fee for converting Flexible Staked VERTO to Fixed-Term Staked VERTO?

No. There are no additional fees for moving VERTO from flexible staking to fixed-term staking, only gas fees.

### What happens at the end of the lock duration? What is "After Burning"?

When your fixed-term staking period ends, and your VERTO unlocks, you have 7 days to complete one of two options:

* Lock your VERTO to begin a new fixed-term staking period\
  or
* Convert your staked VERTO to flexible staking (no 72-hour withdrawal fee).
![Convert staked VERTO to flexible staking](/public/assets/locked-lock-ended-before-after-burning.png)

During these 7 days, you will still earn VERTO.

After 7 days, if you have not done one of the two options, your staked VERTO will enter what is called "After Burning". With "After Burning", your VERTO rewards will start to be sent to burn. The % of VERTO rewards being sent to burn will linearly increase in the 90 days "After Burning" period until it reaches 100%, which means all the VERTO rewards are burnt.

So, to avoid missing out on VERTO rewards, we recommend starting a new fixed-term staking period or converting your VERTO to flexible staking at the end of your lock staking period.

![](/public/assets/locked-lock-ended-after-burning-started.png)
