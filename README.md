# Range-Join-Non-Equijoin-and-mapping-table
Range Join / Non-Equijoin and mapping table

The type of join used in your example is often referred to as a **range join** or a **non-equijoin**.

### Key Concepts:

1. **Range Join / Non-Equijoin**:
   - A **range join** (or **non-equijoin**) occurs when the join condition involves a range of values rather than an exact match. In your case, you are using conditions like `price >= min_price AND price <= max_price` to join the `products` table with the `discounts` table, rather than using equality (`=`) as in a typical equi-join.
   - This kind of join is useful when one table has continuous or overlapping ranges (e.g., price ranges, score ranges, or date ranges), and you need to find which range a value from another table falls into.

2. **Tables**:
   - **Lookup Table** (e.g., `discounts`): The `discounts` table is functioning as a **lookup table** in this case. It defines certain ranges (e.g., price ranges) and associates each range with a value (in this case, a `discount_rate`).
     - Lookup tables are commonly used for categorizing data, such as mapping ranges of values (like price or marks) to categories (like discounts or grades).
   - **Fact Table** (e.g., `products`): The `products` table is providing the actual data (in this case, product information and prices). It can be thought of as a **fact table** in data modeling, which stores the primary data that needs to be categorized or analyzed.

### Characteristics of a **Range Join**:
- **Join condition involves inequalities** (`>=`, `<=`, `BETWEEN`).
- **Matches rows based on ranges** of values rather than exact equality.
- **Common in scenarios like**:
  - Price ranges (as in your example)
  - Date ranges (e.g., finding which time period a date falls into)
  - Score or grade ranges (e.g., mapping test scores to letter grades)

### Other Types of Joins (for comparison):
- **Equi-Join**: A typical join where the condition is an equality (e.g., `ON table1.id = table2.id`).
- **Self-Join**: A join where a table is joined with itself.
- **Left Join, Right Join, Outer Join**: Joins that include all rows from one table even if there is no match in the other table.
  
In this case, because you are joining based on a range of values rather than an exact match, the join is specifically a **range join** or **non-equijoin**.

Let me know if you need more details or further clarification!
