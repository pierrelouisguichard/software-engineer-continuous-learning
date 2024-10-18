# SQL

## Records and Fields

![Row and Columns](./assets/RowAndColumns.PNG)

rows are records and columns are fields

## Comments

```sql
-- This is a comment

/*
This is a
block comment
*/
```

## Sort (ORDER BY)

```sql
SELECT *
FROM movies
ORDER BY year ASC -- ascending by default (123)
```

```sql
SELECT *
FROM movies
ORDER BY year DESC -- descending (321)
```

## Limit (LIMIT)

```sql
SELECT *
FROM movies
LIMIT 10
```

## Skip records (OFFSET)

```sql
SELECT *
FROM movies
LIMIT 3 OFFSET 2
```

## Alias (AS)

```sql
SELECT movie_title AS title
FROM movies
```

## Join strings (CONCAT)

```sql
SELECT CONCAT(first_name, last_name) AS full_name
FROM employees
```

## Filter (WHERE)

```sql
SELECT *
FROM studio
WHERE name = 'Walt Disney'
```

## Unique (DISTINCT)

```sql
SELECT DISTINCT department
FROM employees
```

## String length (CHAR_LENGTH())

```sql
SELECT tweet_id
FROM Tweets
WHERE char_length(content) > 15;
```
