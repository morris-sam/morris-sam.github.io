---
layout: default
---
# OM 620 - Inventory Safety Stock Calculation

For most organizations, inventory management is one of the most critical operational tasks. Inventory management is the task of understanding, managing, and maintaining quantities of inventory. This management task often involves analytical undertakings, such as inventory forecasting, determining optimal order quantities, supplier selection, and warehouse optimization, among others.

To make data-driven decisions, inventory managers often deal with an excessive amount of raw, uncleaned, and disjointed data that needs to be cleaned, harmonized, and standardized before undertaking any analysis.

These assignments tackle the analytical challenges of calculating the safety stock value for individual stock-keeping units (SKUs) that are designated as make-to-stock inventory type.

Files containing this can be found [in my OM-620 repository](https://github.com/morris-sam/OM-620).

The transactional data and metadata are stored in the `Data` folder, and the assignments are stored in the `Notebook` folder. These have been tested on Python 3.14.10 with no issues.

Needed Python packages: Pandas and SciPy.

## Assignment 1:

This assignment deals with cleaning the provided data, largely those that seemed anomalous or were missing values.

| Column Name          | Anomaly Type        | Number of Entries | Change Made                                            |
|:---------------------|:--------------------|:------------------|:-------------------------------------------------------|
| `sku_number`         | Empty Values        | 170               | Replaced with "Missing"                                |
| `inventory_type`     | Empty Values        | 9,389             | Replaced with "Missing"                                |
| `stocking_type`      | Empty Values        | 21,555            | Replaced with "Missing"                                |
| `lead_time`          | Out of the ordinary | 10                | Replaced values of "2800" with "28", assuming misinput |
| `unit_price`         | Out of the ordinary | 10                | Replaced negative price with their absolute value      |
| `manufacturing_site` | Empty Values        | 152,425           | Replaced with "Missing"                                |
| `division_code`      | Empty Values        | 54,888            | Replaced with "Missing"                                |
| `transaction_date`   | Incorrect Data Type | All               | Converted values from "String" to "DateTime"           |
| `order_quantity`     | Out of the ordinary | 40,358            | Replaced negative quantities with their absolute value |

The assignment further analyzed which country transactions took place in based on their manufacturing site.

Filtering by finished goods in the "make to stock" category in the provided data, the following conclusions have been drawn:
- 368 unique SKUs
- 20 unique manufacturing sites
- 55 divisions
- The transaction with the most units and was the highest in sales was SKU Number `BB9C0690` with an order quantity of 187 units and a sales value of $188,555.54, and took place on November 18th, 2025.

## Assignment 2:

This assignment calculated the safety stock for "make to stock" SKUs based on the transformed data from the previous assignment. Service levels of 75%, 90%, and 95% were used.

It was calculated that SKU `F39BBC11` has the highest required safety stock for each service level, with 152 units at 75%, 288 units at 90%, and 370 units at 95%.

It was calculated that SKU `2462CBBC` has the lowest required safety stock for each service level, with 13 units at 75%, 24 at 90%, and 31 units at 95%.

Across all the SKU's, the average safety stock is 51 units at 75%, 97 units at 90%, and 125 units at 95%.

However, the initial forecasting assumed that the demand was normally distributed, which may not be the case. Separately, safety stock was calculated with the daily demand quantiles, yielding different results.

While it may depend on the item in particular, both methods were calculated to see which SKUs had demand that was normally distributed, and which did not.
