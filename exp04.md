<div align="center">
  <h1>SQL Lesson 4: Filtering and sorting Query results</h1>
</div>

*Question 1:-* List all directors of Pixar movies (alphabetically), without duplicates
```sql
SELECT DISTINCT Director
FROM Movies
ORDER BY Director ASC;
```

*Question 2:-* List the last four Pixar movies released (ordered from most recent to least)
```sql
SELECT *
FROM Movies
ORDER BY Year DESC
LIMIT 4;
```

*Question 3:-* List the first five Pixar movies sorted alphabetically
```sql
SELECT *
FROM Movies
ORDER BY Title ASC
LIMIT 5;;
```

*Question 4:-* List the next five Pixar movies sorted alphabetically
```sql
SELECT *
FROM Movies
ORDER BY Title ASC
LIMIT 5 OFFSET 5;
```