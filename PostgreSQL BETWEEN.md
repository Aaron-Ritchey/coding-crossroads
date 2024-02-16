#languages/PostgreSQL 

```postgresql

-- This is fine. --
Prices.start_date <= purchase_date AND purchase_date <= Prices.end_date

-- This is how the cool kids do it. --
purchase_date BETWEEN Prices.start_date AND Prices.end_date
```