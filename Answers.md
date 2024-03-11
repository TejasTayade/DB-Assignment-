Q 1  Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Ans: Two entities "product" and "Product_Category" from given diagram related to each other in ONE-TO-MANY relationship. 
     A product can belong to one category (indicated by the category_id foreign key in the Product table), 
     but a category can have many products.  This is reflected in the cardinalities (numbers) at the end of the connector line in the diagram: 
     "one" on the Product_Category side and "many" on the Product side.

Q 2   How could you ensure that each product in the "Product" table has a valid category assigned to it?
Ans:  With the help of following way we can ensure that each product in "Product" table has a valid category assigned to it:
      Database Constraints:
      Foreign Key Constraint: This is the most common approach. 
      The category_id in the Product table can be set as a foreign key referencing the id of the Product_Category table. 
      This enforces database level validation. Any attempt to insert a product with an invalid category ID (one that doesn't exist in the Product_Category table) will fail.
      Check Constraint: We can add a check constraint on the category_id column in the Product table. 
      The constraint can be a query that verifies the existence of the referenced category ID in the Product_Category table.



      
