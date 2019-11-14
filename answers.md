1, 
SELECT *  FROM `employees` WHERE `firstName` LIKE 'M%' ORDER BY `officeCode` DESC

2, 

SELECT
	e.firstName, 
    e.LastName, 
    c.city
FROM employees e
LEFT JOIN offices c
ON e.officeCode = c.officeCode
 WHERE e.employeeNumber = 1501

3,

SELECT 
    lastName, firstName
FROM
    employees
WHERE
    officeCode IN (SELECT 
            officeCode
        FROM
            offices
        WHERE
            country = 'USA')
