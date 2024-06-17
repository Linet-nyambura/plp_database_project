# netflix data used on this project
- I downloaded the database as told, and imported it on my sql workbench.On importing i changed the database table name to time spent.
- This where my challenge came into.since,on using the SELECT* FROM time spent and ran a query,i only got an error.
- Until i realized that i had to use SELECT * FROM `time spent` which ran successfully and ended up even changing the table name to table_spent to avoid the trailing spaces that lead to an error.
## interesting part about the data
- i ran a number of COUNT(*) functions on the data and group and order the data based on what i had selected example, SELECT gender,COUNT(*) FROM time_spent group by gender ORDER BY gender ASC, others i grouped by platform, others i selected,grouped and order on gender, plaform,profession all combined and i realized the results on count kept on changing.Though for platforms,ie, SELECT platform, COUNT(*) FROM time_spent GROUP BY platform ORDER BY platform asc; that facebook had 307 counts, Instagram 363 count and youtube 330.
- i also loved how the professions were balanced between the various platforms and gender also.