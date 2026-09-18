Complex Economic Behavior & Financing Modes

This repository contains a NetLogo agent-based model simulating macroeconomic consumption under the influence of complex, peer-driven behavior. The model explores how different structural financing mechanisms—specifically interest-based lending versus markup financing—affect systemic stability, wealth distribution, and aggregate debt.

Overview
In this model, an agent's consumption is determined not only by their personal income and net wealth, but also by the average consumption of their spatial neighbors. This peer-induced pressure often forces agents to seek external financing to maintain social parity. The model evaluates three distinct financial frameworks to service this demand:

Interest-Free Lending: Baseline transfer with no capital growth.

Interest-Based Lending: Debt acts as an income-generating asset for the lender, allowing for refinancing and exponential debt growth.

Markup Financing: Financing is strictly tied to actual consumption, prohibiting the refinancing of past debt and preventing creditors from profiting from delayed payments.

Theoretical Framework & System Dynamics
The Interest-Based Paradigm: By treating debt itself as an income-generating asset, the model creates an explosive positive feedback loop. Lenders earn interest, driving their personal consumption higher, which pulls the neighborhood average up with it. This forces neighboring agents deeper into debt. Because refinancing and compounding are permitted, debt disconnects from real resources and grows exponentially until the cycle is reset by bankruptcy.

The Markup Paradigm: This mode acts as a structural circuit breaker. By restricting financing strictly to real, tangible consumption and prohibiting the refinancing of previous debt, the vicious borrowing cycle is blocked. Because creditors cannot profit from delayed payments, they have an endogenous incentive to cap exposure (e.g., limiting the amount due to 50% of average income) to prevent defaults. This risk-sharing alignment ties financial expansion directly to the real economy, resulting in systemic stability, higher fund utilization, and robust aggregate savings.

Wealth Transfers (Charity): Because consumption is linked spatially across neighbors, wealth transfers from high net-worth agents to lower net-worth agents do not merely act as localized relief. They stabilize local consumption averages, mitigating peer-induced borrowing pressure and optimizing the systemic environment for both donors and receivers.

Prerequisites
NetLogo: Version 7.0.4 or higher.

Usage & Configuration
Open the .nlogox file in NetLogo and use the interface sliders to configure the economic environment before clicking setup and go.

Selecting a Mode of Finance
Interest-Free Model: Set r = 0 and m = 0.

Interest-Based Model: Set r to a positive value (e.g., 0.06 for 6%). Ensure m = 0.

Markup Model: Set m to a positive value (e.g., 0.06). Ensure limit-amount-due is toggled On. This protects creditors by capping the amount-due at 50% of the agent's average income, avoiding delays in payment. (Note: You cannot have both m and r greater than zero simultaneously).

Key Economic Parameters
relativity: Controls the weight of peer influence. A value of 0.5 means 50% of an agent's desired consumption is dictated by personal income/wealth, and 50% is dictated by the neighborhood average.

std-r: The standard deviation of the relativity parameter across the agent population.

income-propensity / wealth-propensity: The marginal propensity to consume out of income and wealth, respectively.

z: A charity/donation parameter representing the percentage of wealth transferred from above-average net-worth agents to those in need. To isolate the impact of charity, toggle allow-lending to Off.

Consistency Checks
The model includes rigorous macroeconomic accounting safeguards to ensure validity:

Total sources of funds must exactly equal total uses (income + loan + charity - consumption - surplus = zero).

Total shares of agents in accumulated surplus must equal 1.0.

Aggregate net wealth of the economy strictly equals total cash (debt and credit cancel each other out).

Credits & References
The theoretical foundation of this model is based on the following research:

Al-Suwailem, Sami (2008). Islamic Economics in a Complex World, Islamic Development Bank.

Al-Suwailem, Sami (2011). Behavioural Complexity, Journal of Economic Surveys, vol. 25.

Al-Suwailem, Sami (2013). Simulation in Islamic Economics, presentation at Mohammadia School of Engineering.

The Lorenz curve and Gini Index graph implementations are adapted from the NetLogo Models Library: Wealth Distribution, (c) Uri Wilensky.
