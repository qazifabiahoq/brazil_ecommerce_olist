

# Impact of Seller Offer Prioritization on Customer Satisfaction

## Project Overview

This project evaluates whether implementing a new **seller offer prioritization algorithm** can improve customer satisfaction among **single-order buyers** on the **Olist e-commerce platform**. The objective is to determine if this change can **increase satisfaction**, encourage **repeat purchases**, and ultimately **drive revenue growth**.

## Who Will Benefit

* **Olist Business Teams**: Gain insights into buyer behavior to refine seller ranking and product recommendation strategies.
* **Product Managers**: Understand the impact of backend offer prioritization changes on user experience and satisfaction.
* **Data Science & Analytics Teams**: Leverage validated experimental design and statistical testing methods.
* **Sellers on Olist**: Learn how product volume and diversity affect satisfaction outcomes.
* **E-commerce Strategists**: Explore how algorithmic changes can be used to target high-impact customer segments.

## Objective

To test the hypothesis that prioritizing seller offers differently can positively influence satisfaction among first-time customers, who make up **93% of Olist’s customer base**.

### Hypotheses

* **Null (H₀)**: Seller offer prioritization has no impact on satisfaction for single-order customers.
* **Alternative (H₁)**: Seller offer prioritization increases satisfaction for single-order customers.

## Summary of Methodology

* **Target Audience**: 37,770 single-order customers who purchased from the **top five product categories**:

  * `cama_mesa_banho` (bed, table & bath)
  * `beleza_saude` (beauty & health)
  * `esporte_lazer` (sports & leisure)
  * `moveis_decoracao` (furniture & decoration)
  * `informatica_acessorios` (computers & accessories)

* **Data Filtering**: Only orders that were:

  * Successfully delivered
  * Had valid customer review scores
  * Belonged to known Brazilian states

* **Stratification Variables**:

  * **Customer state** (geographic region)
  * **Product category**
  * **Seller ID**
  * Ensured balance between **test** and **control** groups using stratified random sampling (n=31,140)

* **Experiment Groups**:

  * **Control group (n=15,570)**: Existing seller offer system
  * **Test group (n=15,570)**: New seller offer prioritization logic

## Key Findings

### 1. Customer Satisfaction Distribution

* **Control group satisfaction** (Score ≥ 4): **75.44%**
* **Test group satisfaction** (Score ≥ 4): **74.84%**
* **Chi-square test**: No statistically significant difference (χ² = 1.79, p = 0.1812)

### 2. Repeat Purchase Behavior

* No statistically significant difference in repeat purchases between groups (p = 1.0)
* Important to note: this is based on historical data without the new algorithm fully implemented

### 3. Geographic Influence

* Strong regional variations observed:

  * **Highest satisfaction**: Tocantins (4.13), São Paulo (4.10)
  * **Lowest satisfaction**: Bahia (3.77), Rio de Janeiro (3.76)
* Significant differences in delivery rates by state (χ² = 154.13, p < 0.001)
* Justified need for geographic stratification

### 4. Product Category Insights

* **Highest satisfaction**:

  * `perfumaria` and `brinquedos` (4.16)
  * `beleza_saude` (4.14)
  * `esporte_lazer` (4.11)
* **Lowest**: `cama_mesa_banho` (\~3.90)

### 5. Seller Characteristics

* Sellers with more products (\~24) had higher average satisfaction (4.03)
* High-priced products (up to R\$895) were correlated with greater variability in satisfaction
* Balanced seller representation helped avoid bias

## Experimental Design Details

* Stratification across **state**, **category**, and **seller**
* Ensured **balance**:

  * **Geographic balance**: No statistically significant difference (χ² = 9.28, p = 0.9989)
  * **Category balance**: Each major category equally represented (\~18–26%)
  * **Seller balance**: Top sellers equally represented across both groups (±2%)

## Conclusion

The experiment was carefully designed and validated with rigorous statistical controls. While **no significant impact** of the new seller offer prioritization on short-term customer satisfaction or repeat purchases was observed, the **balanced and unbiased experimental setup** provides a strong foundation for further testing.

### Recommendations

* **Run A/B test in production** with real-time seller offer prioritization to evaluate long-term effects
* **Monitor key KPIs**: Repeat purchase rate, satisfaction score trends, and average order value
* Consider **category-specific optimizations** and **state-level personalization** in future iterations

## Dataset Details

* Total unique customers analyzed: **37,770**
* Orders included: **Delivered**, **Reviewed**, **Known location**
* Categories: Top 5 by order volume
* Customers per group: **15,570 (control)**, **15,570 (test)**

