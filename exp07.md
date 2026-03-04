<div align="center">
  <h1>SQL Lesson 6: Multi-table queries with JOINs</h1>
</div>

*Question 1:-* Find the domestic and international sales for each movie
```sql
SELECT Movies.Title, Boxoffice.Domestic_sales, Boxoffice.International_sales
FROM Movies
JOIN Boxoffice
ON Movies.Id = Boxoffice.Movie_id;
```

*Question 2:-* Show the sales numbers for each movie that did better internationally rather than domestically
```sql
SELECT Movies.Title, Boxoffice.Domestic_sales, Boxoffice.International_sales
FROM Movies
JOIN Boxoffice
ON Movies.Id = Boxoffice.Movie_id
WHERE Boxoffice.International_sales > Boxoffice.Domestic_sales;
```

*Question 3:-* List all the movies by their ratings in descending order
```sql
SELECT Movies.Title, Boxoffice.Rating
FROM Movies
JOIN Boxoffice
ON Movies.Id = Boxoffice.Movie_id
ORDER BY Boxoffice.Rating DESC;
```