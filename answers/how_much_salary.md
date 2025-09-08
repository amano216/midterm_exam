## emp_noが40000の従業員の1996年~1997年にかけての給料を教えてください。

### 答え
132506

### SQL
```sql
USE employees; SELECT SUM(salary) FROM salaries WHERE emp_no = 40000 AND from_date >= '1996-01-01' AND from_date < '1998-01-01';
```
