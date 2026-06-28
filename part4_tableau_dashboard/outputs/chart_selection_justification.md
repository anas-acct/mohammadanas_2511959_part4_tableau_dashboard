# Chart Selection Justification

**1. Sales Trend (Line Chart)**
*   **Question Answered:** How are sales changing over time?
*   **Why it's appropriate:** Line charts are the universal standard for displaying continuous time-series data, making trends and seasonality instantly visible.
*   **Fields Used:** `Order Date` (Columns), `Sales` (Rows).
*   **Design Principle:** Clean layout. I removed unnecessary gridlines to focus the eye on the trend.
*   **Mistake Avoided:** Avoided using a bar chart for time, which would make the view cluttered and harder to read sequentially.

**2. Regional Performance (Filled Map)**
*   **Question Answered:** Which regions perform best?
*   **Why it's appropriate:** Maps leverage spatial recognition, allowing executives to immediately see geographical clusters of success or failure.
*   **Fields Used:** `State` (Detail), `Profit` (Color).
*   **Design Principle:** Meaningful colors. By using a sequential color palette, high-profit states naturally pop out.
*   **Mistake Avoided:** Avoided using a massive text table of 50 states, which takes too long for a human to process.

**3. Category Profitability (Sorted Horizontal Bar Chart)**
*   **Question Answered:** Which categories drive profits or losses?
*   **Why it's appropriate:** Bar charts are best for comparing categorical data. A horizontal orientation allows long sub-category names to be easily read without tilting the head.
*   **Fields Used:** `Category/Sub-Category` (Rows), `Profit` (Columns/Color).
*   **Design Principle:** Clear hierarchy. Sorting from highest to lowest profit instantly highlights the most and least important products.
*   **Mistake Avoided:** Avoided using a pie chart, which makes it nearly impossible to compare the sizes of 15+ sub-categories accurately.

**4. Discount vs. Profit (Scatter Plot)**
*   **Question Answered:** How does discount relate to profit?
*   **Why it's appropriate:** Scatter plots are the only chart type capable of showing correlation between two distinct numerical measures across multiple dimensions.
*   **Fields Used:** `Discount` (Columns), `Profit Margin` (Rows), `Sub-Category` (Detail).
*   **Design Principle:** Minimal clutter.
*   **Mistake Avoided:** Avoided aggregating all discounts into a single bar, which would hide the specific impact on individual sub-categories.
