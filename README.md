# RBU Employee Database SQL

## 1. Create the Table

```sql
CREATE TABLE RBU (
    empld INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    dept TEXT NOT NULL
);
```

This command creates a table named `RBU`.

### Columns

| Column  | Description                 |
| ------- | --------------------------- |
| `empld` | Employee ID and Primary Key |
| `name`  | Employee name               |
| `dept`  | Employee department         |

### Constraints

* `PRIMARY KEY` ensures that every employee has a unique ID.
* `NOT NULL` ensures that the employee name and department cannot be empty.

## 2. Insert Employee Records

```sql
INSERT INTO RBU VALUES (1001, 'AMAN', 'Sales');
INSERT INTO RBU VALUES (1002, 'ROHIT', 'EXECUTIVE');
INSERT INTO RBU VALUES (1003, 'KARAN', 'INDUSTRY EXECUTIVE');
```

These statements insert three employees into the `RBU` table.

The table now contains:

```text
+-------+-------+-------------------+
| empld | name  | dept              |
+-------+-------+-------------------+
| 1001  | AMAN  | Sales             |
| 1002  | ROHIT | EXECUTIVE         |
| 1003  | KARAN | INDUSTRY EXECUTIVE|
+-------+-------+-------------------+
```

## 3. Search for SMART Department

```sql
SELECT * FROM RBU WHERE dept = 'SMART';
```

At this point, there is no employee in the `SMART` department.

### Output

```text
Empty set
```

This happens because no record currently has `dept = 'SMART'`.

## 4. Insert a SMART Department Employee

```sql
INSERT INTO RBU VALUES (1004, 'NIKHIL', 'SMART');
```

This adds NIKHIL with employee ID `1004` to the `SMART` department.

## 5. Search for SMART Department Again

```sql
SELECT * FROM RBU WHERE dept = 'SMART';
```

Now the query finds NIKHIL.

### Output

```text
+-------+--------+-------+
| empld | name   | dept  |
+-------+--------+-------+
| 1004  | NIKHIL | SMART |
+-------+--------+-------+
```

## Final Table

After all the commands are executed, the `RBU` table contains four employees:

```text
+-------+--------+-------------------+
| empld | name   | dept              |
+-------+--------+-------------------+
| 1001  | AMAN   | Sales             |
| 1002  | ROHIT  | EXECUTIVE         |
| 1003  | KARAN  | INDUSTRY EXECUTIVE|
| 1004  | NIKHIL | SMART             |
+-------+--------+-------------------+
```
