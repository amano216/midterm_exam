## emp_noが49988の従業員の最初の役職(title)はなんですか？

### 答え
Assistant Engineer

### SQL
```sql
USE employees; SELECT title, from_date FROM titles WHERE emp_no = 49988 ORDER BY from_date ASC LIMIT 1;
```
