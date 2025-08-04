## Total Shows by Rating
```sql
SELECT
  rating AS Rating,
  COUNT(show_id) AS Total_Shows
FROM netflix GROUP BY rating ORDER BY Total_Shows DESC;
```
| Rating | Total_Shows |
| -------------------- | -------------------- |
| TV-MA | 2027| 
| TV-14 | 1698| 
| TV-PG | 701| 
| R | 508| 
| PG-13 | 286| 
| NR | 218| 
| PG | 184| 
| TV-Y7 | 169| 
| TV-G | 149| 
| TV-Y | 143| 
| TV-Y7-FV | 95| 
| G | 37| 
| UR | 7| 
| NC-17 | 2| 

## Top 10 Genre by Total Shows
```sql
SELECT
  listed_in AS Genre,
  COUNT(show_id) AS Total_Shows
FROM netflix GROUP BY listed_in ORDER BY Total_Shows DESC
LIMIT 10;
```
| Genre | Total_Shows |
| -------------------- | -------------------- |
| Documentaries | 299| 
| Stand-Up Comedy | 273| 
| Dramas, International Movies | 248| 
| Dramas, Independent Movies, International Movies | 186| 
| Comedies, Dramas, International Movies | 174| 
| Kids' TV | 159| 
| Documentaries, International Movies | 150| 
| Children & Family Movies, Comedies | 129| 
| Children & Family Movies | 120| 
| Comedies, International Movies | 120| 

## Movies and TV-Shows Distribution by Total Shows
```sql
SELECT
  type AS Show_Type,
  COUNT(show_id) AS Total_Shows
FROM netflix GROUP BY type;
```
| Show_Type | Total_Shows |
| -------------------- | -------------------- |
| Movie | 4265| 
| TV Show | 1969| 

## Total Movies and TV-Shows by Year
```sql
SELECT
  type AS Show_Type,
  release_year AS Year,
  COUNT(show_id) AS Total_Shows
FROM netflix 
WHERE release_year>=2010 AND release_year<=2020
GROUP BY type, release_year;
```
| Show_Type | Year | Total_Shows |  Show_Type | Year | Total_Shows |
| -------------------- | -------------------- |-------------------- |  -------------------- | -------------------- |-------------------- |
| Movie | 2010 | 111|  TV Show| 2010| 38| 
| Movie| 2011| 100|  TV Show| 2011| 36| 
| Movie| 2012| 125| TV Show| 2012| 58| 
| Movie| 2013| 177| TV Show| 2013| 60| 
| Movie| 2014| 213| TV Show| 2014| 75| 
| Movie| 2015| 363| TV Show| 2015| 154| 
| Movie| 2016| 593| TV Show| 2016| 237| 
| Movie| 2017| 682|  TV Show| 2017| 277| 
| Movie| 2018| 646| TV Show| 2018| 417| 
| Movie| 2019| 400| TV Show| 2019| 443| 
| Movie| 2020| 6| TV Show| 2020| 19|

## Total Movies and TV-Shows by Country
```sql
SELECT
  type AS Show_Type,
  country AS Country,
  COUNT(show_id) AS Total_Shows
FROM netflix 
GROUP BY type, country;
```
| Show_Type | Year | Total_Shows |  Show_Type | Year | Total_Shows |
| -------------------- | -------------------- |-------------------- |  -------------------- | -------------------- |-------------------- |
| Movie | 2010 | 111|  TV Show| 2010| 38| 
| Movie| 2011| 100|  TV Show| 2011| 36| 
| Movie| 2012| 125| TV Show| 2012| 58| 
| Movie| 2013| 177| TV Show| 2013| 60| 
| Movie| 2014| 213| TV Show| 2014| 75| 
| Movie| 2015| 363| TV Show| 2015| 154| 
| Movie| 2016| 593| TV Show| 2016| 237| 
| Movie| 2017| 682|  TV Show| 2017| 277| 
| Movie| 2018| 646| TV Show| 2018| 417| 
| Movie| 2019| 400| TV Show| 2019| 443| 
| Movie| 2020| 6| TV Show| 2020| 19|
