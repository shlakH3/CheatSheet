
# ---Table users---
id |name                 |age|birth_place                         |birth_day |is_admin|
3  |Jeffrey Boone        |  3|Iraq                                |2018-04-10|       0|
9  |Evan Schmidt         | 20|Japan                               |2001-12-06|       0|
10 |Brian Irwin          | 45|Maldives                            |1976-04-13|       0|
11 |Benjamin Barrera     | 49|Falkland Islands (Malvinas)         |1972-03-19|       0|
12 |Lisa Hernandez       |  1|Netherlands                         |2020-12-28|       1|
13 |Brandi Jone          |  7|Iran                                |2014-04-29|       0|
-----------------
---Table numbers---
id |
1  |
2  |
3  |
4  |
5  |
20 |
30 |
-------------------

・Display id" is from users table.
・WHERE cluase displays when the result is true(1).
-----------------------------------------------------------------------------------------
# Display All records of users table
SELECT * FROM users;

# Display ASC (id 11=>13=>10=>9=>3=>12)
SELECT * FROM users ORDER BY name;

# Display DESC (id 12=>3=>9=>10=>13=>11)
SELECT * FROM users ORDER BY name DESC;

# Display only id 9
SELECT * FROM <tableName> WHERE age = "20";

# Display id 3,9,12,13
SELECT * FROM <tableName> WHERE age BETWEEN 3 AND 20;

# Display id 10,11,12
SELECT * FROM <tableName> WHERE age NOT BETWEEN 3 AND 20;

# Display id 10,11,13
SELECT * FROM <tableName> WHERE name LIKE "B%";

# Display id 3,13
SELECT * FROM <tableName> WHERE name LIKE "%ne";

#Display id 3,9,13
SELECT * FROM users WHERE age IN(3,20,7);
#Display id 3=>13=>9
SELECT * FROM users WHERE age IN(3,20,7) ORDER BY age;

# Display id 10,11,12
SELECT * FROM users WHERE age NOT IN(3,20,7);

# Display id 3
SELECT * FROM users WHERE id IN(SELECT id FROM numbers);

# Display none
SELECT * FROM users WHERE id > ALL(SELECT id FROM numbers);

# Display id 9,10,11,12,13 
SELECT * FROM users WHERE id > ALL(SELECT id FROM numbers WHERE id < 9);
*****
SELECT id FROM numbers WHERE id < 9   => id 1,2,3,4,5 
=> SELECT id FROM numbers WHERE id > 1,2,3,4,5
*****

# Display id 3
SELECT * FROM users WHERE id < ANY(SELECT id FROM numbers WHERE id < 9);
*****
SELECT id FROM numbers WHERE id < 9   => id 1,2,3,4,5 
=> SELECT id FROM numbers WHERE id < 1 
=> SELECT id FROM numbers WHERE id < 2 (1)
=> SELECT id FROM numbers WHERE id < 3 (1,2)
=> SELECT id FROM numbers WHERE id < 4 (1,2,3)
=> SELECT id FROM numbers WHERE id < 5 (1,2,3,4)
*****

# Display id 13
SELECT * FROM users WHERE age > 3 AND birth_place = "Iran";

# Display id 3,10,11
SELECT * FROM users WHERE age > 20 OR birth_place = "Iraq";

###Display###
---Table users---
id |name             |age|
3  |Jeffrey Boone    |6
#############
SELECT id, name, age+3 FROM users WHERE name LIKE "J%";

###Display###
3:Jeffrey Boone
9:Evan Schmidt
10:Brian Irwin
11:Benjamin Barrera
12:Lisa Hernandez
13:Brandi Jone
#############
SELECT CONCAT(id,":",name) FROM users;

# Display 2024-12-22 17:43:04
SELECT NOW();

# Display 2024-12-22
SELECT CURDATE();

# Display 2024/12/22
SELECT DATE_FORMAT(NOW(),"%Y/%m/%d");

# Display |ABC   | (Delete only blank space on the left side)
SELECT LTRIM("   ABC    ");

# Display |   ABC| (Delete only blank space on the right side)
SELECT RTRIM("   ABC    ");

# Display |ABC| (Delete blank space on both sides)
SELECT TRIM("    ABC    ");

# Display "BCD"
SELECT SUBSTR("ABCDE",2,3);

###Display### 
---Table users---
id |name |
3  |Jeffr|
#############
SELECT id, SUBSTRING(name,1,5) FROM users WHERE id = 3;

# Display "EDCBA"
SELECT REVERSE("ABCDE");

# Display "3"
SELECT ROUND(3.14);

# Display "3.1"
SELECT ROUND(3.14,1);

# Display "350"
SELECT ROUND(345,-1);

# Display "3"
SELECT FLOOR(3.14);

# Display "4"
SELECT CEILING(3.14);

# Display 81 (3*3*3*3)
SELECT POWER(3,4)
-----------------------------------------------------------------------------------------
