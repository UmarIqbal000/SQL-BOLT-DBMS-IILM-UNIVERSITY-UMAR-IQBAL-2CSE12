<div align="center">
  <h1>SQL Review: Simple SELECT Queries</h1>
</div>

*Question 1:-* List all the Canadian cities and their populations
```sql
SELECT City, Population
FROM north_american_cities
WHERE Country = 'Canada';
```

*Question 2:-* Order all the cities in the United States by their latitude from north to south
```sql
SELECT City
FROM north_american_cities
WHERE Country = 'United States'
ORDER BY Latitude DESC;
```

*Question 3:-* List all the cities west of Chicago, ordered from west to east
```sql
SELECT City
FROM north_american_cities
WHERE Longitude < -87.6298
ORDER BY Longitude ASC;
```

*Question 4:-* List the two largest cities in Mexico (by population)
```sql
SELECT City, Population
FROM north_american_cities
WHERE Country = 'Mexico'
ORDER BY Population DESC
LIMIT 2;
```

*Question 5:-* List the third and fourth largest cities (by population) in the United States and their population
```sql
SELECT City, Population
FROM north_american_cities
WHERE Country = 'United States'
ORDER BY Population DESC
LIMIT 2 OFFSET 2;
```