# netflix data used on this project
- I downloaded the database as told, and imported it on my sql workbench.On importing i changed the database table name to time spent in the workbench.
- This where my challenge came into.since,on using the SELECT* FROM time spent and ran a query,i only got an error.
- Until i realized that i had to use SELECT * FROM `time spent` which ran successfully and ended up even changing the table name to table_spent to avoid the trailing spaces that lead to an error.

## interesting part about the data
- i ran a number of COUNT(*) functions on the data and group and order the data based on what i had selected example, SELECT gender,COUNT(*) FROM time_spent group by gender ORDER BY gender ASC, others i grouped by platform, others i selected,grouped and order on gender, plaform,profession all combined and i realized the results on count kept on changing.Though for platforms,ie, SELECT platform, COUNT(*) FROM time_spent GROUP BY platform ORDER BY platform asc; that facebook had 307 counts, Instagram 363 count and youtube 330.
- i also observed they was a variance in income levels by location just by a quick observation.
- i also loved how the professions were balanced between the various platforms and gender also.
- i also realized that the average indebt based on demographics was zero ,this after using SELECT demographics, AVG(indebt) AS avg_indebt FROM time_speny GROUP BY de,ographics ORDER BY demographics;...Thus Rural, Sub_urban and Urban each had an avg_indebt of 0.
- i also realized that the total income of users by location was 5,292,969 in Autralia, 4,975,000 in United Kingdom and 4,746,854 in United States ..this after running the following query, SELECT location, SUM(income) AS total_income FROM time_spent GROUP BY location ORDER BY total_income DESC;
- i also realized the most time spent was 9 by all genders, male, female and non_binary on using SELECT gender, time_spent FROM time_spent GROUP BY gender, time_spent ORDER BY gender desc, time_spent desc;
- it's interesting also since i realized that the overall average income based on the SELECT DISTINCT income ROUND(AVG(income) OVER(), 0) AS avg_income FROM time_spent ORDER BY income; was 15015 a hiddenn fact for sure
- I also realized that the maximum income 19,980 whch apparently was a marketer manager and the minimum income was 10012 which was for a student..overall i mean using the SELECT MIN(income), MAX(income) FROM time_spent.
### questions
- i asked myself the platform with the highest average time spent.and after runing a query using SELECT platform, AVG(time_spent) AS avg_time_spent FROM time_spent GROUP BY platform ORDER BY avg_time_spent DESC; I note it was 5.1515 for instagram, 5.0554 for facebook and 4.8697 for youtube
- i was also curious what was the average time spent on social media by age group,so i run the query,SELECT age, AVG(time_spent) AS avg_time_spent FROM time_spent GROUP BY age ORDER BY age.since its a bigger list i found that the average time spent based on age were between 4.00 to 6.19
- i also wanted to know the average income coorelated with the time spent so i ran the query, SELECT location, AVG(income) AS avg_income, AVG(time_spent) AS avg_time_spent FROM time_spent GROUP BY location ORDER BY location; and realized that average income was 15036.8438, 15121.5805 and 14880.4201 while average time spent was 5.2188, 4.9088 and 4.9436 for Autralia, United Kingdom and United States respectively.

### pitch deck ,excel and word links 
<a href = "https://docs.google.com/spreadsheets/d/15th1pzMOIzZK-W4q1H1uHkGfq1W-CRw3NMeyHG2dQLE/edit?usp=sharing">EXCEL LINK</a>.It contain my projects visualization
<a href = "https://docs.google.com/presentation/d/1nN8NM120I9fAjernBcW7z-4dzsjH9P51GgOGZriuQyo/edit?usp=sharing">PITCH DECK</a>.Its on the above project
<a href="https://docs.google.com/document/d/1HCgMUC5oB039obNvWtgF4UFJxruEM6dBkesBJyAl6pc/edit?usp=sharing">MS WORD</a>.It contain some of my sql queries used on the above project.

