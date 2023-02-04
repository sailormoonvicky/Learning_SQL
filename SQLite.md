
# SQLite function

1. strftime()\
It takes two arguments:
strftime(format, column)
```
  SELECT timestamp,
    strftime('%H', timestamp)
  FROM hacker_news
  GROUP BY 1
  LIMIT 20;
```
This returns the hour, ```HH```, of the ```timestamp``` column!

For ```strftime(__, timestamp)```:

- ```%Y``` returns the year (YYYY)
- ```%m``` returns the month (01-12)
- ```%d``` returns the day of the month (1-31)
- ```%H``` returns 24-hour clock (00-23)
- ```%M``` returns the minute (00-59)
- ```%S``` returns the seconds (00-59)
if ```timestamp``` format is ```YYYY-MM-DD HH:MM:SS```.
