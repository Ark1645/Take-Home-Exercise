Of course. Here is a comprehensive `README.md` file crafted using the specific Markdown syntax you provided.

-----

# NovaTech Digital Shelf Diagnostic & Performance Audit

This repository contains the complete analysis and deliverables for a diagnostic investigation into the root causes of revenue fluctuations for our client, **NovaTech Electronics**. The project synthesizes disparate e-commerce data points to produce a *prioritized* list of actionable insights and strategic recommendations.

## Analytical Approach

To diagnose the complex relationship between increased ad spend and volatile revenue, we implemented a four-phase analytical methodology designed to audit NovaTech's digital presence holistically.

  * **Data Aggregation & Synthesis**: The initial phase involved ingesting and consolidating five distinct data sources—including performance metrics, inventory movements, and marketplace snapshots—into a unified analytical model.
  * **Profitability & Performance Modeling**: We moved beyond surface-level metrics to model true profitability. By integrating `cost_basis`, we calculated **Profit After Ad Spend (PAAS)**, offering a clear view of which products were generating actual margin.
  * **Multi-Point Digital Shelf Audit**: We systematically scanned for common e-commerce pitfalls across three critical domains:
      * *Availability & Inventory Health*
      * *Pricing & Channel Compliance*
      * *Content & Brand Reputation*
  * **Insight Prioritization & Reporting**: All identified issues were categorized and ranked using a priority framework. The final output is a structured JSON report designed for easy integration into business intelligence workflows.

## Key Discoveries & Strategic Recommendations

The audit uncovered several high-impact issues directly contributing to financial leakage and suppressed performance.

  * **Critical Finding \#1: Significant Ad Spend Leakage on an Out-of-Stock Product**

      * **Discovery**: The **NT-TABLET-P6** is listed as *“temporarily\_unavailable”* on Amazon. Despite this, NovaTech spent **$4,500 on advertising** for this product, driving 5,800 clicks to an unpurchaseable page.
      * **Recommendation**: **Immediately pause all advertising campaigns** for the NT-TABLET-P6. Implement a stock-aware advertising protocol to automatically pause campaigns for any OOS product.

  * **Critical Finding \#2: Revenue Siphoning via Lost Buy Box on a Core Product**

      * **Discovery**: NovaTech is losing the Amazon Buy Box for its **NT-SPEAKER-Z2** to a third-party seller, "FastShip Electronics". This product is also flagged with *"low\_stock,"* with only 12 units available.
      * **Recommendation**: Investigate the cause of the Buy Box loss and **expedite replenishment of FBA inventory** for this SKU.

  * **Critical Finding \#3: Unsustainable Ad Strategy Eroding Margin on a Flagship Product**

      * **Discovery**: The flagship **NT-EARBUD-X1** generated a **negative profit of -$354.58** on Amazon. Its ROAS has been in steady decline, falling to just 1.38, indicating a highly inefficient campaign.
      * **Recommendation**: Conduct an urgent, in-depth audit of the **NT-EARBUD-X1** ad campaigns to restore profitability.

## Priority Framework

Insights are categorized to guide immediate action and strategic planning.

  * **P1 (High)**: Issues causing direct, significant, and ongoing financial loss. *Requires immediate intervention.*
  * **P2 (Medium)**: Issues eroding profitability, suppressing conversion rates, or creating competitive vulnerabilities. *Requires prompt review.*
  * **P3 (Low)**: Foundational issues and optimization opportunities that impact long-term growth.

## How to Run the Analysis

  * **Prerequisites**: Ensure Python 3.8+ and pip are installed.
  * **Install Dependencies**: From the project root, run:
    ```python
    pip install -r requirements.txt
    ```
  * **Run the Script**:
    ```python
    python scripts/main.py
    ```
  * The script will generate a report named `diagnostic_report.json` in the `outputs/` directory.

## Assumptions Made

  * The `identifier` in `performance_metrics.csv` correctly maps to the `item_code` in `internal_catalog_dump.csv`.
  * The `cost_basis` provided in the catalog data accurately represents the per-unit Cost of Goods Sold (COGS).
  * The marketplace snapshot is the most current representation of the digital shelf state.

## AI Usage Disclosure

This project was developed with the assistance of an AI tool ([Visit Google](https://gemini.google.com)). The AI was utilized for:

  * *Initial Script Scaffolding*
  * *Logic Implementation for the multi-point audit*
  * *Documentation Drafting*

All AI-generated outputs were reviewed, tested, and refined by the author to ensure correctness and alignment with the project's strategic objectives.

## Future Enhancements

  * **Automated Monitoring & Alerting**: Convert the script into an automated service that runs daily and sends real-time alerts.
  * **Predictive Demand Forecasting**: Leverage historical data to build a model that predicts stockout risks.
  * **Competitive Intelligence Dashboard**: Create a live dashboard that tracks key competitors' pricing, promotions, and review velocity.
