# About stEVER

Liquid staking is a new method of income accrual for EVER token holders. With it, you no longer have to lock tokens for a specific period of time in order to receive rewards. Turning on to the liquid staking option, you can do both at once. Namely, stake EVER, receive stEVER (staked EVER) tokens in return, and participate in DeFi to generate additional yield or in EVER DAO to vote for proposals.

The work to integrate stEVER into EVER DAO is underway.

### Let’s see how it works

stEVER is a TIP 3.1 token with the same characteristics as other tokens launched on Everscale. They are issued and deposited on your wallet balance the moment you stake your EVER in the system. The number of stEVER received in return is determined by the current exchange rate **(see how it forms below)**. In turn, the amount of EVER you will receive by unstaking changes in line with the accruals of EVER awards. The validators of stEVER work as the usual ones, except that their depools receive stakes only from the **balancer**.

### The Balancer mechanism

When users stake with depools, they are willing to get the most out of a pool’s APR. However, it changes depending on the amount of liquidity and the number of users staking. The rates fluctuate daily, and depending on how long you lock your tokens for, you could end up getting much less back than you initially imagined.

The launch of stEVER tokens drastically reduces this risk with the help of a **balancer mechanism**. It is designed to keep the APR as high as possible. Currently, it is close to the basic profitability of the network. To do so, the balancer manages the stakes distribution between depool contracts. It ensures that the rounds are not overloaded and that pools work at peak efficiency.

### The formulas

$$i$$ - epoch number

$$rate_i$$ - exchange rate after deposit/withdrawal&#x20;

$$E_i$$ - new total stEVER supply

$$C_i$$ - new cumulative stEVER collateral in EVERs

$$c_i$$ - amount of EVERs that are withdrawn at the stEVER burning (unstaking)

$$r_i$$ - epoch reward in EVERs

$$e_i$$ - how many stEVERs are to be issued (exchanged) after the deposit of EVERs

* The amount of stEVERs issued in return for staked EVERs:

$$
e_i= \frac{E_{i-1} *c_i}{C_{i-1}}
$$

* New total stEVER supply:

$$
E_i=E_{i-1}+e_i
$$

* New cumulative stEVER collateral in EVERs:

$$
C_i=C_{i-1}+c_i+r_i
$$

* The exchange rate of stEVER and EVER after stacking/unstaking:

$$
rate_i=\frac{E_i}{C_i},i>0
$$

* The amount of EVERs that are withdrawn at the stEVER burning (unstaking):

$$
c_i=\frac{E_{i-1}*e_i}{C_{i-1}}
$$

