## emp_noが40000の従業員の1996年~1997年にかけての給料を教えてください。

### 答え
128935

### SQL
```sql
USE employees;

SELECT
  ROUND(SUM(
    salary * DATEDIFF(
      LEAST(to_date, '1998-01-01'),
      GREATEST(from_date, '1996-01-01')
    ) / DATEDIFF(to_date, from_date)
  )) AS total_salary
FROM salaries
WHERE emp_no = 40000
  AND to_date > '1996-01-01'
  AND from_date < '1998-01-01';

```
