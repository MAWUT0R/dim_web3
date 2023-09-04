### Introduction
Vesta Finance is a platform that provides overcollateralized stablecoin loans on Arbitrum. With ETH, ARB, GMX, and more, users could take loans in VST, Vesta’s native stablecoin, up to a minimum collateralization ratio of 110%. This means that a user with $1,000 worth of underlying collateral in a vault can borrow (issue) up to 909.09 VST, which is freely exchangeable between wallets with or without an open vault at Vesta. In this piece, we’ll be making an in-depth assessment of Vesta Finance, including its stablecoin peg mechanism, liquidations, and overall operations of the debt platform.

### Peg Mechanism
The VST stablecoin’s peg is maintained by borrowers (arbitrageurs) who find incentives in restoring the price to $1 amid volatility. For example, if VST’s price increases >$1, borrowers could make an instant profit by borrowing the maximum amount against their collateral and selling VST on the market for profit. Conversely, if VST’s prices decrease <$1, the Vesta Reference Rate increases exponentially, making it expensive to hold VST. This encourages borrowers to buy back VST, pay back their loans, and close vaults. This decreases the VST in circulation and increases its price.

### Liquidations & The Stability Pool
When borrowers’ vaults fall below the minimum collateral ratio (MCR), Vesta performs liquidations using the stability pool in either of these two conditions:

- If the stability pool is not empty, undercollateralized vaults are sold against the stability pool containing VST tokens.
- If the stability pool is empty, a Vest bot will estimate and redistribute undercollateralized vaults to other borrowers.
  
In essence, Vesta uses the VST tokens in the stability pool to absorb the liabilities of under-collateralized borrowers. Users can also choose to deposit VST tokens into the stability pool to earn liquidated collateral. To incentivize participation, stability pool providers are rewarded with VSTA tokens in an event known as “community issuance”.

### Mobilizing Collateral
Deposited collateral in vaults can sometimes be mobilized to generate yield on the side. However, for staking opportunities to be considered, they must meet the following conditions:

- Immediate withdrawal - Vaults could be called anytime during user interaction or liquidation so funds have to be readily withdrawable at any point in time.
- Security - Staked assets are only deposited into highly secure and proven strategies to ensure some degree of recoverability.
All GMX and GLP tokens deposited by users are immediately deposited into the native GMX staking system to capture yield.

### Savings Module
Users looking to earn a fee can lock up their VST for a period of time to earn an interest rate. The rate is funded by the Vesta Reference Rate collected from borrowers. The locked-up VST is used to backstop the stability pool during liquidations.

### Fee Revenue
Vesta generates revenue from two main sources:

- Staking revenue from mobilizing collateral.
- Vesta reference rate paid in VST.

### Vesta Emergency Reserve
The Emergency Reserve is a fund set aside to make users whole in the case of a shortfall event. Fees in the ecosystem as well as future fees all accrue to the Emergency Reserve. Shortfall events include smart contract risk, liquidation risk, oracle failure risk, or any case of loss of capital.

### VSTA Tokenomics
VSTA is used to incentivize stability pool participation and is also used for protocol governance purposes. VSTA tokens were initially distributed between the community, contributors, and partners. Here’s the breakdown:

- Community Treasury (63%)
- Core Contributors (21%)
- Advisors (4%)
- Strategic Partners (6%)
- Treasury Bootstrapping (4%)
- Whitelisting (1%)
- Olympus DAO (1%)

### Conclusion
Vesta Finance is a promising DeFi lending protocol that offers a number of features that make it attractive to users. These features include:

- Overcollateralized loans, which help to reduce the risk of default.
- A stablecoin peg mechanism that is designed to keep the value of VST stable at $1.
- Liquidations that help to protect the value of VST and the stability pool.
- A saving module that allows users to earn interest on their VST.
- A fee revenue model that is designed to be sustainable in the long term.
- An emergency reserve that protects users in the event of a shortfall event.
  
Overall, Vesta Finance is a well-designed protocol that has the potential to be a major player in the DeFi lending space. However, it is still a relatively new project, and it will be important to monitor its performance over time to see how it fares in the real world.
