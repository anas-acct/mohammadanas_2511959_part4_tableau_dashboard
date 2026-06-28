## Data Assumptions (Task 1)
* **Geographic Scope**: The geographic fields (`state` and `city`) represent the Indian market.
* **Return Flag**: The `return_flag` column is treated as a binary categorical dimension where `1` indicates a returned order and `0` indicates a completed, non-returned order.
* **Monetary Values**: Financial metrics (`sales` and `profit`) are assumed to be in the local currency (INR) and do not require conversion.
* **Discount Format**: The `discount` field is a decimal representation of a percentage (e.g., 0.1 = 10%).
* **Data Completeness**: It is assumed there are no critical missing values in the key dimensions required for executive decision-making.
