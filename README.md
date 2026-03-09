# RFM Dashboard

An **RFM (Recency, Frequency, Monetary) customer segmentation dashboard**.

This project summarizes customer behavior into clear segments (e.g., “Champions”, “At Risk”, etc.) and provides interactive visuals to explore marketing/retention insights.

## Data Privacy / Synthetic Dataset

This repository uses a **synthetic (fake) dataset**.

The original version of this work was built using private customer/order data. That private data is **not included** here. All examples and outputs shown in this repository are generated from synthetic data that does **not** represent any real individuals, accounts, or transactions.

## What this dashboard does

At a high level, the dashboard workflow is:

1. **Ingest transactional data** (orders / invoices / payments, etc.)
2. **Compute RFM features** per customer:
   - **Recency**: how recently they purchased
   - **Frequency**: how often they purchased
   - **Monetary**: how much they spent
3. **Score and segment customers** using RFM thresholds/quantiles
4. **Visualize** segments and explore distributions/drilldowns

## Screenshots / Walkthrough

### 1) Overview / Main dashboard view

<img width="1432" height="855" alt="Screenshot 2026-03-07 at 18 39 20" src="https://github.com/user-attachments/assets/d45b9b64-1c47-4820-ad59-03ce6f0d9a07" />

**What you’re seeing:**
- A top-level summary of customer segmentation based on RFM scoring.
- High-level KPIs that typically answer questions like:
  - How many customers are active vs. dormant?
  - Which segments contribute the most revenue?
  - How does customer value break down across segments?

**Why it matters:**
This view is meant for quick “health check” monitoring and identifying which segments deserve attention (retain, win-back, upsell, etc.).

---

### 2) Segment distribution / breakdown view

<img width="1434" height="851" alt="Screenshot 2026-03-07 at 18 47 32" src="https://github.com/user-attachments/assets/b8af6802-7037-412c-958f-330d3ff3b738" />

**What you’re seeing:**
- A deeper breakdown of the population across RFM segments.
- Visuals that typically show:
  - Segment sizes (counts and percentages)
  - Segment revenue contribution
  - Comparison across dimensions (e.g., recency buckets vs. frequency buckets)

**Why it matters:**
This view helps prioritize operational actions. For example:
- A growing “At Risk” segment might suggest churn risk.
- A strong “Champions” segment can be targeted for loyalty/referral campaigns.

---

### 3) Detail / drill-down view (segment or customer-level exploration)

<img width="1438" height="853" alt="Screenshot 2026-03-07 at 18 48 01" src="https://github.com/user-attachments/assets/056434c8-4d2e-4718-a4e4-3280af3d4b6b" />

**What you’re seeing:**
- A more detailed exploration view intended for drill-down:
  - Filtering into a segment
  - Inspecting distributions (spend, order counts, last purchase date)
  - Validating whether the segmentation logic “makes sense” in the data

**Why it matters:**
This is the “analysis” view: it supports decision-making by letting you inspect what’s driving a segment (e.g., customers are “At Risk” because recency is high even if spend is strong).

## Notes / Assumptions

- Segment names and cutoffs can vary widely by business context. In real deployments, thresholds are usually tuned and validated with domain input.

---