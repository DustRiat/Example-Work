/*
This is a basic mini-project for
the Codecademy Learn SQL course.
This code shows the requested queries
for the Startups analysis.
*/

SELECT COUNT(name)
FROM startups;

--Total value of all companies
SELECT SUM(valuation)
FROM startups;

--Which company raised the highest amount during seed stage
SELECT name, MAX(raised)
FROM startups
WHERE stage = 'Seed';

--Oldest startup on this list
SELECT name, MIN(founded)
FROM startups;

--Average valuation by startup category
SELECT category, ROUND(AVG(valuation),2)
FROM startups
GROUP BY 1
ORDER BY 2 DESC;

--Most competitive startup markets by category
SELECT category, COUNT(*)
FROM startups
GROUP BY 1
HAVING COUNT(*) > 3
ORDER BY 2 DESC;

--Average size of startups in different locations
SELECT location, category, ROUND(AVG(employees),0)
FROM startups
GROUP BY location
HAVING AVG(employees) > 500
ORDER BY employees DESC;
