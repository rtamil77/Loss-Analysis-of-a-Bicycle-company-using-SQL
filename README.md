# 🚲 Loss Analysis of Adventure Works Bicycle Company Using SQL

## 📌 Project Overview

**Adventure Works** is a manufacturing company that produces bicycles and bicycle-related products. The company operates across several functional areas, including:

- 🏭 Production
- 💰 Sales
- 📦 Procurement
- 👥 Customer and Person Management
- 🧾 Inventory Management
- 🚚 Sales Territory Management

The company’s product portfolio includes bicycles, components, accessories, and clothing. This project analyzes Adventure Works sales data using **SQL** to identify the major sources of loss and provide data-driven recommendations to improve overall profitability.

---

## 🏢 Business Background

Adventure Works manufactures and sells a wide variety of products. The products are primarily grouped into four major categories:

| Category | Description |
|:--|:--|
| 🚲 Bikes | Finished bicycle products sold to customers |
| ⚙️ Components | Bicycle parts and mechanical components |
| 🎒 Accessories | Additional bicycle-related products |
| 👕 Clothing | Apparel and clothing products |

These four categories are further divided into:

| Level | Count |
|:--|--:|
| Product Categories | 4 |
| Product Subcategories | 37 |
| Product Models | 128 |
| Total Products | 504 |
| Categorized Finished Products | 295 |
| Uncategorized / Unfinished Products | 209 |

Out of the total **504 products**, only **295 products** belong to a product category, subcategory, or model. These are treated as finished goods.

The remaining **209 products** do not belong to a category, subcategory, or product model. These products are considered unfinished goods.

---

## 🎯 Business Problem

Adventure Works wants to improve profitability by identifying the causes of losses across its sales operations.

The objective of this analysis is to understand:

- Which products generate the highest profit and loss
- Which product models, subcategories, and categories create losses
- Which customer types are more profitable
- Which customers generate the highest sales
- Which years, quarters, and months have the highest profit or loss
- Which sales territories perform better or worse
- How discounts affect profit and loss
- Whether promotions and clearance sales are profitable
- Which products require pricing, production, or promotion changes

---

## 🔍 Analysis Areas

The sales data was analyzed from multiple perspectives.

### 📦 Product Analysis

- Product-level profit and loss
- Product model performance
- Product category performance
- Product subcategory performance
- Loss-making products and product groups

### 👥 Customer Analysis

- Retail customer performance
- Wholesale customer performance
- Individual customer performance
- Store customer performance
- Customer sales contribution
- Profitability by customer type

### 📅 Time-Based Analysis

- Profit and loss by year
- Profit and loss by quarter
- Profit and loss by month
- Seasonal sales and loss patterns

### 🌎 Territory Analysis

- Sales performance by sales territory
- Profitability by region
- Loss-making territories

### 💸 Discount Analysis

- Impact of discounts on profitability
- Clearance-sale performance
- Promotion-sale performance
- No-discount sales performance
- Markup percentage analysis

---

## 👥 Customer Segment Findings

Adventure Works sells finished products to two primary customer groups:

| Customer Type | Percentage of Customers | Percentage of Sales | Profitability Observation |
|:--|--:|--:|:--|
| 🛍️ Retail Customers | 93.25% | 20% | Generates more profit and does not create significant loss |
| 🏪 Wholesale Customers | 6.75% | 80% | Generates more loss than profit |

### Key Observation

Retail customers represent **93.25% of the overall customer base**, but they contribute only **20% of total sales**.

Wholesale customers represent only **6.75% of customers**, but they contribute approximately **80% of total sales**.

Although wholesale customers generate more loss than profit, reducing wholesale sales is not a practical solution because wholesale customers account for the majority of company sales.

```text
Retail Customers
├── 93.25% of total customers
├── 20% of total sales
└── More profitable with little or no loss

Wholesale Customers
├── 6.75% of total customers
├── 80% of total sales
└── Higher sales contribution but more loss than profit
```

Therefore, the company should not simply reduce its wholesale customer base. Instead, Adventure Works should identify the product groups and discount strategies that cause losses within wholesale sales.

---

## 🚨 Major Loss-Making Subcategories

After analyzing sales, profit, discounts, and product performance, three bicycle subcategories were identified as major contributors to loss:

| Rank | Subcategory | Primary Cause of Loss | Recommendation |
|:--:|:--|:--|:--|
| 1 | 🚵 Mountain Bikes | Clearance sales caused by excess inventory | Reduce production and align inventory with demand |
| 2 | 🚲 Touring Bikes | Promotion sales are generating significant losses | Reassess promotion strategy and promotional discounts |
| 3 | 🏍️ Road Bikes | Negative or insufficient markup, even without discounts | Review pricing and markup strategy |

---

# 📊 Detailed Findings and Recommendations

## 🚵 Mountain Bikes

### Finding

Mountain Bikes are profitable overall, but a significant amount of loss occurs through **Clearance Sales**.

Clearance sales generally indicate that inventory is not moving at the expected rate. In this case, Adventure Works may be producing more Mountain Bikes than customers are purchasing.

```text
Higher Production
        ↓
Excess Inventory
        ↓
Slow-Moving Stock
        ↓
Clearance Sale
        ↓
Reduced Margin / Loss
```

### Business Impact

When excess inventory is sold through clearance sales:

- 📉 Selling prices are reduced
- 💸 Profit margins decrease
- 📦 Inventory holding costs may increase
- 🏭 Production capacity may be used inefficiently
- 🚲 Overall profitability is negatively affected

### Recommendation

Adventure Works should reduce the production volume of Mountain Bikes and align production more closely with actual sales demand.

Recommended actions:

- Use historical sales trends to forecast Mountain Bike demand.
- Reduce overproduction of slow-moving Mountain Bike models.
- Monitor inventory turnover more frequently.
- Introduce early-warning thresholds for excess inventory.
- Use targeted pricing strategies before products require clearance discounts.
- Analyze regional and seasonal demand before planning production.

> 💡 **Recommendation:** Mountain Bikes remain profitable overall, but reducing clearance-sale losses can significantly increase total profit.

---

## 🚲 Touring Bikes

### Finding

Touring Bikes generate considerable losses through **Promotion Sales**.

The analysis shows that promotional discounts on Touring Bikes do not generate sufficient additional profit to justify the cost of the promotion.

```text
Promotion Discount
        ↓
Lower Selling Price
        ↓
Reduced Profit Margin
        ↓
Insufficient Increase in Sales Volume
        ↓
Overall Loss
```

### Business Impact

The current promotion strategy may be ineffective because:

- 📉 Promotional discounts reduce the selling price.
- 💸 The margin reduction is greater than the additional revenue gained.
- 🚲 Promotion sales do not create enough incremental demand.
- 📊 The promotion may attract lower-margin sales rather than new profitable customers.

### Recommendation

Adventure Works should reassess the promotion strategy for Touring Bikes.

Recommended actions:

- Reduce promotion discount percentages.
- Test promotions by region, customer segment, and season.
- Compare promoted sales against non-promoted sales.
- Use targeted promotions instead of broad discount campaigns.
- Bundle Touring Bikes with accessories instead of heavily discounting the bike itself.
- Use loyalty rewards, financing offers, or free services instead of direct price reductions.
- Measure incremental profit, not only sales volume, for every campaign.

> 💡 **Recommendation:** Promotion sales for Touring Bikes should be redesigned because the current promotions are creating losses without delivering sufficient profit.

---

## 🏍️ Road Bikes

### Finding

Road Bikes generate the **highest loss** among the identified bicycle subcategories.

The most important finding is that the loss occurs even when there is **No Discount** applied.

```text
No Discount Applied
        ↓
Loss Still Occurs
        ↓
Selling Price Is Too Low or Cost Is Too High
        ↓
Negative / Insufficient Markup
        ↓
Loss-Making Road Bike Sales
```

If Road Bikes are being sold at a loss without any discount, the underlying problem is likely the pricing or markup configuration.

The analysis indicates that markup percentages for some Road Bike products are negative.

### Business Impact

Negative markup means that the selling price is less than the product cost.

```text
Selling Price < Product Cost
        ↓
Negative Markup
        ↓
Loss on Every Sale
```

This is especially critical because the loss is not caused by promotional discounts. It indicates a fundamental issue with product pricing, product cost, or margin calculation.

### Recommendation

Adventure Works should immediately review the markup percentage and pricing strategy for Road Bikes.

Recommended actions:

- Review the cost price and selling price of every Road Bike product.
- Identify all Road Bike models with negative markup.
- Recalculate product cost, including manufacturing, labor, logistics, and overhead.
- Increase selling prices where appropriate.
- Set minimum-margin rules for Road Bike sales.
- Prevent products from being sold below cost unless specifically approved.
- Review wholesale pricing contracts and customer-specific pricing.
- Evaluate whether certain Road Bike models should be redesigned, discontinued, or sourced differently.

> 💡 **Recommendation:** Road Bike pricing and markup must be reviewed urgently because losses occur even when no discounts are applied.

---

# ✅ Final Recommendations

Based on the analysis, the following actions are recommended to increase Adventure Works profitability:

| Priority | Recommendation | Expected Benefit |
|:--:|:--|:--|
| 🔴 High | Review Road Bike pricing and negative markup percentages | Prevents losses on regular, non-discounted sales |
| 🔴 High | Reduce Mountain Bike overproduction | Reduces excess inventory and clearance-sale losses |
| 🔴 High | Redesign Touring Bike promotions | Reduces losses caused by ineffective discounts |
| 🟠 Medium | Analyze wholesale pricing and margins | Improves profitability from the customer segment contributing 80% of sales |
| 🟠 Medium | Create product-level margin monitoring | Identifies loss-making products early |
| 🟠 Medium | Implement inventory-demand forecasting | Improves production planning and inventory turnover |
| 🟢 Medium | Use targeted discounts instead of broad promotions | Protects margins while supporting sales |
| 🟢 Medium | Monitor profitability by territory and customer type | Helps identify high-value and high-risk sales segments |

---

# 🏁 Conclusion

The analysis shows that Adventure Works can improve profitability by focusing on the root causes of loss rather than reducing sales from wholesale customers.

Although wholesale customers generate more loss than profit, they also contribute approximately **80% of total sales**. Therefore, removing or reducing wholesale customers would negatively affect revenue.

The more effective approach is to address the loss-making product subcategories:

1. 🚵 **Mountain Bikes**  
   Reduce overproduction to avoid inventory buildup and clearance-sale losses.

2. 🚲 **Touring Bikes**  
   Reassess promotional discounts because promotion sales are generating significant losses.

3. 🏍️ **Road Bikes**  
   Review pricing and markup immediately because losses occur even when no discounts are applied.

By improving inventory planning, discount management, promotion effectiveness, and product-level pricing, Adventure Works can reduce losses and increase overall profitability.

---

## 🧰 Tools Used

```text
SQL
Adventure Works Database
Data Analysis
Profit and Loss Analysis
Sales Analysis
Customer Segmentation
Discount Analysis
Product Performance Analysis
```
