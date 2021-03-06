# CRUD Quiz

Use the solution to this afternoon's Property Tracker lab to answer the following questions. Please write your answers under each question, push the file to GitHub, and submit in the usual way.

## MVP Questions

In our Property Tracker application:

Q1. Where are we instantiating instances of the `Property` class?

 Is in my 'models/property.rb' when we are using the initialize method with all the properties of the class Property.

Q2. Where are we defining the SQL that enables us to save the ruby `Property` object into the database?

In property.rb

Q3. In console.rb, which lines modify the database?

All those using methods as delete, save, all, find.

so, lines 4, 13, 22, 31, 33, 35, 37, 39

Q4. Why do we not define the id of a `Property` object at the point we instantiate it (‘new it up’)?

Beacuse SQL will do it in the table if we request it, also if we assign this as a property it will require to be added manually, which will be a never ending task if there was lots of data objects.

Q5. Where and how do we assign the id (that is generated by the database) to the ruby `Property` object?

 In 'property.rb' when adding 'id' as a property of an instance 'property class' and we instantiate 'id' as follows:

 <!-- for that we add this to the initialize method @id = options['id'].to_i if options['id'] --> then, add id the the table properties in the database as a PRIMARY KEY.


Q6. Why do we put a guard (an `if` clause) on the `@id` attribute in the constructor?

To gain access to id with the attr_reader from the database if there is any id produced by sql.

Q7. Why are some of the CRUD actions represented by instance methods, and others by class methods?

because instance methods modify or use part of the instance values added to the database, while class methods modify or display the whole class data storage in our database.


Q8. What type of data structure is returned by calls to `db.exec_prepared()`? In the `save` method, how do we access the id from the returned data structure?

It gives back a Progress result of an object, and we access it by the attr_reader.

Q9. Why do we use prepared statements when performing database operations?

sql = "SELECT * FROM database filename WHERE id = placeholder for id"

## Extension Questions

Look at the `find_by_id` and `find_by_address` methods in the `Property` class.

Q10. What do they take in as their arguments?

The id and address array values assigned to a variable called values.

Q11. What are their return values?
