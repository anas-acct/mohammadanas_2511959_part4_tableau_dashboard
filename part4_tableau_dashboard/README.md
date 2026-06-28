## Data Assumptions (Task 1)
* **Geographic Scope**: The geographic fields (`state` and `city`) represent the Indian market.
* **Return Flag**: The `return_flag` column is treated as a binary categorical dimension where `1` indicates a returned order and `0` indicates a completed, non-returned order.
* **Monetary Values**: Financial metrics (`sales` and `profit`) are assumed to be in the local currency (INR) and do not require conversion.
* **Discount Format**: The `discount` field is a decimal representation of a percentage (e.g., 0.1 = 10%).
* **Data Completeness**: It is assumed there are no critical missing values in the key dimensions required for executive decision-making.

## Calculated Fields Created (Task 2)
To enable deeper executive analysis, the following calculated fields were created:

1. **Profit Margin**: `SUM([profit]) / SUM([sales])` (Formatted as %)
   * *Purpose*: To measure profitability relative to revenue.
2. **Cost**: `[sales] - [profit]`
   * *Purpose*: To isolate the raw cost of goods sold.
3. **Average Order Value (AOV)**: `SUM([sales]) / COUNTD([order_id])`
   * *Purpose*: To track customer purchasing behavior and basket size.
4. **Return Rate**: `COUNTD(IF [return_flag] = 1 THEN [order_id] END) / COUNTD([order_id])` (Formatted as %)
   * *Purpose*: To monitor product quality and customer satisfaction issues.
5. **Shipping Delay Bucket**: Grouped `[delivery_days]` into Fast (0-1), Standard (2-3), Delayed (4-5), and Very Delayed (6+).
   * *Purpose*: To visualize supply chain efficiency and identify shipping bottlenecks.
