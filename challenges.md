
1. Show all the psql users. (Hint: Look for a command to show roles)
  * \du

2. Show all the tables in your apartmentlab database.
 * \dt

3. Show all the data in the owners table.
 * SELECT * FROM owners

4. Add three owners: Donald (age 56), Elaine (age 24), and Emma (age 36).
 * INSERT INTO owners (name, age) VALUES ('Donald', 56), ('Emma', 36), ('Elaine', 24);

5. Show the names of all owners.
 * SELECT name FROM owners;

6. Show the ages of all of the owners in ascending order.
 * SELECT ages FROM owners ORDER BY age ASC;

7. Show the name of an owner whose name is Donald.
 * SELECT name FROM owners WHERE name = 'Donald';

8. Show the age of all owners who are older than 30.
 * SELECT age FROM owners WHERE age > 30;

9. Show the name of all owners whose name starts with an "E".
 * SELECT name FROM owners WHERE name LIKE 'E%';

10. Add an owner named John who is 33 years old.
* INSERT INTO owners (name, age) VALUES ('John',33);

11. Add an owner named Jane who is 43 years old.
 * INSERT INTO owners (name, age) VALUES ('Jane', 43);

12. Change Jane's age to 30.
 * UPDATE owners SET age = 30 WHERE name = 'Jane';

13. Change Jane's name to Janet.
 * UPDATE owners SET name = 'Janet' WHERE name = 'Jane';

14. Delete the owner named Janet.
 * DELETE FROM owners WHERE name = 'Janet' RETURNING *;

15. Add a property named Archstone that has 20 units.
 * INSERT INTO properties (name, num_units) VALUES ('Archstone', 20);

16. two more properties with names and number of units of your choice.
 * INSERT INTO properties (name, num_units) VALUES ('Bedrock', 89), ('GeoDome',2);

17. Show all of the properties in alphabetical order that are not named Archstone.
 * SELECT * FROM properties WHERE name <> 'Archstone';

18. Count the total number of rows in the properties table.
 * SELECT COUNT(name) FROM properties;

19. Show the highest age of all the owners.
 * SELECT MAX(age) FROM owners;

20. Show the names of the first three owners in your owners table.
 * SELECT name FROM owners LIMIT 3;

21. Use a FULL OUTER JOIN to show all of the information from the owners table and the properties table.
 * SELECT * FROM owners FULL OUTER JOIN properties ON owners.id = properties.person_id;

Stretch Challenges





