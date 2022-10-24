---
category: defi
---

> SoK: systematization of knowledge

**AMM**  
Pros: Provides liquidity and encourage swapping assets \
Cons: Slippage will easily occur. vulnerable to impermanent loss(divergence loss). Also has security issue

A lot of models were proposed to solve this issue, but there were mostly just the same. \
The purpose of this paper is SoK of AMM-based DEX

**Actors**

1. Liquidity Providers
2. Traders
3. Protocol Foundation

**Assets**

1. Risk assets
   - Illiquidity, type of assets the DEX is designed for
2. Base assets
   - In some protocols, risk assets have to be designated with base assets
3. Pool shares
   - Liquidity shares, LP shares. Represents ownership in the portfolio of the assets within a pool
4. Protocol tokens
   - Governance token.

**Dynamics**

1. Invariant properties
   - conservation function. ex) CPMM
2. Mechanisms
   - asset swapping & liquidity provision/withdrawls

**Economy**

1. Rewards
   - Liquidity reward - Receive trading fees
   - Staking reward - Rewards from staking pool shares or other tokens as part of an initial incentive program from a certain token protocol
   - Governance right - rights to vote for proposals
   - Security reward - bounty programs, auditing, etc.
2. Explicit cost
   - Liquidity withdrawal penalty
   - Swap fee
   - Gas fee
3. Implicit cost
   - Slippage
   - Divergence loss(Impermenant loss)

<img src="../../assets/images/defi-on-blockchain.png" />

**State space representation**  
<img src="../../assets/images/liquidity-provision-and-withdrawal.png" />
<img src="../../assets/images/token-exchange.png" />

state $$\chi$$  
$$\chi = ({\{r_k\}_{k=1,...,n}, \{p_k\}_{k=1,...,n}, C, \Omega})$$

$$r_k = quantity\ of\ token\ k$$  
$$p_k = current\ spot\ price\ of\ token\ k$$  
$$C = conservation\ function\ invariants$$  
$$\Omega = collection\ of\ protocol\ hyperparameters$$

**General rules of AMM-based DEX**

1. Price stays constant for pure liquidity provision and withdrawals
2. Invariants of AMM pool stays constant for pure swapping
   $$ (\{r_k\}, \{p_k\}, \mathcal{C}, \Omega) \xrightarrow{liquidity\ change} (\{r_k\}, \{p_k\}, \mathcal{C}', \Omega)$$  
   $$ (\{r_k\}, \{p_k\}, \mathcal{C}, \Omega) \xrightarrow{swap} (\{r_k'\}, \{p_k'\}, \mathcal{C}, \Omega) $$

- Cisproportionate addition or removal can be viewed as combination of proportionate reserve change plus asset swap
- Swap fees causes $$\mathcal{C}$$ to change. It can be divided into swap and provision

**Generalized formulas**

1. Conservation function (bonding curve)  
   $$\mathcal{C} = C(\{r_k\})$$  
   conservation function for each token $$(r_i - r_o)$$ must be concave, nonnegative, nondecreasing  
   $$Z(\{r_k\};\mathcal{C}) = C(\{r_k\}) - \mathcal{C} = 0$$  
   here, $$\mathcal{C}$$ is determined by initial liquidity provision.  
   For example, if AMM formula is $$XY = k$$, then $$Z = XY - k,\ C(\{r_k\}) = XY,\ \mathcal{C} = k$$
2. Spot exchange rate  
   $$_iE_o(\{r_k\}; \mathcal{C}) = \dfrac{\partial Z(\{r_k\};\mathcal{C})/r_o}{\partial Z(\{r_k\};\mathcal{C})/r_i}$$
3. Swap amount
   input $$x_i$$, output $$x_o$$  
   _a) Update reserve quantities_  
    $$r_i':=R_i(x_i;r_i) = r_i + x_i$$  
    $$r_j' = r_j \ \forall j \neq i,o$$

   _b) Comput new reserve quntity of token o_  
    $$r_o' = R_o(x_i, \{r_k\}; \mathcal{C}) \Leftrightarrow Solving\ Z=0$$

   _c) Compute swapped quntity_  
    $$x_o := X_o(x_i, \{r_k\}; \mathcal{C}) = r_o - r_o'$$

4. Slippage
   $$S(x_i, \{r_k\}; \mathcal{C}) = \dfrac{x_i/x_o}{_iE_o} - 1$$
5. Divergence loss  
   value of token $$o$$ is increased by $$\rho$$ while others stay the same  
   token $$_i$$ is a numeraire.  
   _a) Calculate the original pool value_  
   $$V(\{r_k\}; \mathcal{C}) = \sum_j{_iE_o(\{r_k\}; \mathcal{C}) \cdot r_j }$$

   _b) Calculate the reserve value if held outside of the pool_  
   $$V_{held}(\rho; \{r_k\}, \mathcal{C}) = V(\{r_k\}; \mathcal{C}) + [_iE_o(\{r_k\}; \mathcal{C}) \cdot r_o] \cdot \rho$$

   _c) Obtain re-balanced reserve quantities_  
   $$\rho = \dfrac{_jE_o(\{r_k'\};\mathcal{C})}{_jE_o(\{r_k\};\mathcal{C})} -1$$  
   $$Z(\{r_k'\};\mathcal{C}) = 0$$  
   $$r_k' = R_k(\rho,\{r_k\};\mathcal{C})$$

   _d) Calculate the new pool value_  
   $$V'(\rho,\{r_k'\}; \mathcal{C}) = \sum_j{_iE_j(\{r_k'\};\mathcal{C}) \cdot r_j'}$$

   _e) Calculate the divergence loss_  
   $$L(\rho, \{r_k'\}; \mathcal{C}) = \dfrac{V'(\rho, \{r_k'\}; \mathcal{C})}{V_{held}'(\rho, \{r_k'\}; \mathcal{C})} -1$$
