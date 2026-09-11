# Data Analyst Assessment — Written Answers

## Question 2 — Business Problem, Questions, Hypotheses

**A. Business problem:**
Olist wants to grow revenue and keep customers happy, but management doesn't know
where delivery delays, weak product categories, or regional gaps are quietly hurting
the business. We're using order, delivery, and review data to find where operations
or sales strategy can improve.

**B. Questions the analysis will answer:**
1. Which product categories generate the most revenue, and which ones underperform?
2. Does delivery speed affect how customers rate their experience?
3. Which Brazilian states/regions bring in the most revenue and have the best/worst delivery performance?
4. Is revenue growing, shrinking, or seasonal over the 2016–2018 period?
5. Are there categories with strong sales but poor customer satisfaction that need attention?

**C. Hypotheses to test:**
1. **H1:** Orders delivered later than the estimated delivery date receive lower review scores than orders delivered on time.
2. **H2:** Revenue is concentrated in a small number of states/categories rather than spread evenly (the "80/20" pattern common in retail).

(You can add a third if you want more depth, e.g. "Higher-priced orders take longer to deliver.")

---

## Question 7 — Recommendations (Worksheet: Q7)

Fill in the bracketed numbers using your own results, but the structure and logic below
already works with this dataset:

**Recommendation 1 — Fix delivery reliability in the slowest regions**
- What should be done: Identify the states/carriers with the highest late-delivery rate and prioritize logistics fixes there (renegotiate carrier SLAs, add regional fulfillment options).
- Supporting insight: Late deliveries correlate with lower review scores (Q4/Q5 finding).
- Who acts: Operations/Logistics team.
- Potential outcome: Higher average review scores, fewer complaints, better repeat-purchase rate.
- What to measure: Late-delivery % and average review score, tracked monthly, before vs. after.

**Recommendation 2 — Investigate the "high revenue, low review" category**
- What should be done: Audit sellers in the category with strong sales but weak reviews (quality checks, seller scorecards, or removing repeat offenders).
- Supporting insight: The surprising-result finding in Q5.
- Who acts: Category/Seller management team.
- Potential outcome: Improved reviews without losing revenue in an already-popular category.
- What to measure: Average review score for that category over the following quarter.

**Recommendation 3 — Double down on top-performing states/categories**
- What should be done: Increase marketing spend and seller onboarding in the highest-revenue states and categories, since demand is proven.
- Supporting insight: Revenue concentration findings from Q4.
- Who acts: Marketing and business development team.
- Potential outcome: Incremental revenue growth by feeding demand where it already exists.
- What to measure: Month-over-month revenue growth in the targeted states/categories.

**Prioritization:** Recommendation 1 first (delivery affects satisfaction across the whole business and is the most fixable), then Recommendation 2 (contained, medium effort), then Recommendation 3 (lower risk, incremental growth play).

---

## Question 10 — How I Used AI (Worksheet: Q10)

1. **Which AI tools I used:** Claude (Anthropic) for structuring the analysis approach, writing the Python/Pandas cleaning and analysis code, and drafting the management-facing write-up.
2. **What I used them for:** Picking a suitable public dataset, writing the data-cleaning and merge code across the 9 Olist tables, structuring the insight/recommendation tables, and drafting slide content in plain language.
3. **Example where AI helped:** Writing the multi-table join (orders → items → products → reviews → customers) and the delivery-delay calculation logic saved significant time versus writing it from scratch.
4. **Example where I had to verify/correct an AI-generated result:** [Fill this in honestly once you run it — e.g., "The AI's first version of the outlier check used a fixed price threshold; I changed it to the IQR method after checking it against the actual price distribution," or "I had to manually confirm which category name in cat_summary was the 'surprising' one before writing the Q5 explanation, since that requires my own judgment call, not just code output."]

---

## Presentation Outline (5–7 slides)

**Slide 1 — Business Problem:** Olist wants to grow revenue and improve customer satisfaction, but doesn't have visibility into which categories, regions, or delivery issues are helping or hurting.

**Slide 2 — Data & Methodology:** ~100,000 real orders (2016–2018) from Olist's Kaggle dataset, cleaned and joined across 9 related tables in Python (Pandas), covering orders, products, payments, reviews, and customer location.

**Slide 3 — Key Findings:** Your top 3 headline numbers — e.g. top revenue category, late-delivery impact on reviews, top-performing state. (Fill with real numbers from the notebook.)

**Slide 4 — Deep-Dive Insight:** Walk through the single most important/surprising finding (your Q5 answer) with the supporting chart.

**Slide 5 — Recommendations:** The 3 recommendations from Q7, in priority order.

**Slide 6 — Expected Business Impact:** What improves if these are acted on (better reviews, retained customers, incremental revenue) and how you'd measure it (the "what to measure" column from Q7).

**Slide 7 — Limitations & Next Steps:** No cost/profit data (revenue only), reviews may reflect delivery not product quality, data ends in 2018 so patterns may have shifted. Next step: get current data and cost data to turn this into a profit-based analysis.

---


