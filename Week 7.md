### Lecture 7 (CS50: Introduction to Computer Science)

### SQL for Computer Science

**CSV** files is
- ideal format for visual reason (flat file database)
- portable
- light-weight

**Reading CSV**
```
import csv

# remove duplicate
titles = set()

with open("filename.csv", "r") as file:
  reader = csv.DictReader(file)
  for row in reader:
    title = row["title"].strip().upper()
    titles.add(title)

for title in sorted(titles):
  print(title)
```

**Relational Database**
- like a spreadsheet program that can be interacted with
- using **SQL** code/language
- uses for large scale data

**CRUD**
1. ``CREATE`` or ``INSERT``
2. *READ*-> ``SELECT``
3. ``UPDATE``
4. ``DELETE`` or ``DROP``

**Creating Database File in the Command line**
```
sqlite3 filename.db
.mode csv
.import filename.csv filename

# checking the data type column
.schema
```
- everything you do is on the **sqlite prompt**

**Modifiers**
- AVG
- COUNT
- DISTINCT
- LOWER
- MAX
- MIN
- UPPER
- AS

**Filters**
- WHERE
- LIKE
- ORDER BY
- LIMIT
- GROUP BY

**Relational Database**
- uses *primary keys*
- *foreign keys*
- to link the data rows together

**SQL Injection Attacks** is about writing SQL code to trick your database to behave in a certain way that is not intentional.

**Race Condition** is where two people performing the same actions and update the database at the same time. By making them *atomic*. Can be solved by *begin transactions, commit, rollback*.
