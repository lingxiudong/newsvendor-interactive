# Newsvendor Interactive Simulator

This page illustrates the classic **newsvendor problem**, where a retailer must choose a single order quantity \(q\) before seeing uncertain demand \(D\). In this simulator, demand follows a Normal distribution,
\[
D \sim \mathcal{N}(100, 30^2),
\]
and you can explore how different choices of \(q\) and wholesale price \(w\) affect performance.

## How to use this tool

1. **Adjust the sliders** on the left:
   - **Order quantity \(q\)**: how many units the newsvendor orders.
   - **Wholesale price \(w\)**: what the newsvendor pays the distributor per unit.
   - You can also change **retail price \(p\)** and **unit cost \(c\)** if you want to experiment with different economics.

2. **Watch the metrics update**:
   - **Expected sales** \( \mathbb{E}[\min(D,q)] \)
   - **In-stock probability** \( \mathbb{P}(D \leq q) \)
   - **Fill rate** \( \mathbb{E}[\min(D,q)] / \mathbb{E}[D] \)
   - **Newsvendor profit**, **distributor profit**, and **total supply chain profit**

3. **Interpret the charts** on the right:
   - **Profit vs. Order Quantity**: shows expected profit for the newsvendor, the distributor, and the total supply chain.
   - **Expected Sales vs. Order Quantity**: shows how \( \mathbb{E}[\min(D,q)] \) grows with \(q\).
   - **Service Metrics vs. Order Quantity**: plots in-stock probability and fill rate.
   - **Demand density plot (bottom left)**: shows the Normal demand curve and shades the area \( \mathbb{P}(D \leq q) \), illustrating the in-stock probability at the current \(q\).

4. **Pay attention to the markers**:
   - A **circle marker** shows the **newsvendor’s optimal order quantity**
     \[
     q_N = F^{-1}\left(\frac{p - w}{p}\right),
     \]
     which maximizes the newsvendor’s own expected profit.
   - A **square marker** shows the **supply chain–optimal order quantity**
     \[
     q_{SC} = F^{-1}\left(\frac{p - c}{p}\right),
     \]
     which maximizes total supply chain profit (distributor + newsvendor).

## What to think about

- How does changing **\(w\)** move \(q_N\) relative to \(q_{SC}\)?
- When does the decentralized decision (newsvendor optimal) under-order from the perspective of the whole supply chain?
- How do profit, expected sales, and service metrics differ at \(q_N\) vs. \(q_{SC}\)?

Use this tool to build intuition about **underage vs. overage costs**, **critical fractiles**, and **misalignment between local and system-wide objectives** in supply chains.
