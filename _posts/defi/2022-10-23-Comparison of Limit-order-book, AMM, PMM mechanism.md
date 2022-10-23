---
category: defi
---

**Limit Order Book mechanism**

- peer-to-peer swap (wallstreet-like method)
- Usually off-chain
- Gnosis, dYdX

_pros_

1. fast

_cons_

1. Presence of centralized party
1. Expensive gas fee
1. Hard to bootstrap liquidity( need to have a matching buyer if you want to sell a token )

**AMM(Automated Market Maker)**

- peer-to-pool method
- Algorithm automatically decides price of tokens
- Uniswap , Curve, Balancer, DODO
- Constant Product Market Maker of the form $$XY = k$$ is the most common AMM algorithm

_pros_

1. Easier liquidity provision (No need to find buyers)

_cons_

1. Impermanent loss and slippage occur

**PMM(Proactive Market Maker)**

- Invented by DODO team to reduce impermanent loss and slippage
- Onchain generalization of orderbook trading
- Utilizes oracles to gather accurate market prices. PMM use this information to estimate midprice $$i$$
- Proactively adjusts parameters such as asset ratio and curve slop  
   $$P_{margin} = iR$$  
   $$if\ B < B_0 \rightarrow R = 1 - k + (\dfrac{B_0}{B})^2k$$  
   $$if\ Q < Q_0 \rightarrow R = 1 / (1 - k + (\dfrac{Q_0}{Q})^2k)$$  
   $$else \rightarrow R = 1$$

_pros_

1. Better liquidity and price stability
2. Reduces barrier-to-entry for smaller projects
3. Customizable and free market making
4. Enables crowdpooling
5. Can be reversioned to AMM by setting k to 1
6. Capable of supporting stablecoin trading, as it's virtually identical to Curve
