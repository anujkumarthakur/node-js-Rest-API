Read Instruction Clearly

1.Create a Database and Table
        
   CREATE DATABASE restful_db;
   CREATE TABLE product(
	product_id INT(11) PRIMARY KEY AUTO_INCREMENT,
	product_name VARCHAR(200),
	product_price INT(11) 
	)ENGINE=INNODB; 


//This Record are using for testing purpose to insert data in database
//directly by Query. 

INSERT INTO product(product_name,product_price) VALUES
	('Product 1','2000'),
	('Product 2','5000'),
	('Product 3','4000'),
	('Product 4','6000'),
	('Product 5','7000');

2. Install Dependencies
   npm init
   npm install --save express mysql body-parser

3. Run .js file
   node index.js

4.Testing in Postman
  1. Get All Product(GET)
     http://localhost:3000/api/products
  
  2. Get Single Product (GET)
     http://localhost:3000/api/products/3
  
  3. Create a New Product (POST)
     http://localhost:3000/api/products
     //Select Body tab Enter data json formate like-
     Example-
     {
    	"product_name": "Product 6 Added",
    	"product_price": 6000
     }
   4. Update Product (PUT)
      http://localhost:3000/api/products/2
      copy Above link and paste in postman url tab with product id change data like-
      //Example-this data is fetch from product id 2 change product_name and price click send button and go run mysql query it's worked or not.
      {
    	"product_name": "Product 2 Update",
    	"product_price": 7000
      } 
    
   5. Delete Product (DELETE)
      Example-
      http://localhost:3000/api/products/6
      http://localhost:3000/api/products/7
     //after run above link go and chaeck mysql database datas are deleted or not.
   
  6. Search by Name(GET)
     Example-
       here i am using REGExp. in mysql Query
       Query = "SELECT * FROM product WHERE product_name REGEXP +"'^[abc]'";";
      http://localhost:3000/api/product/?
       

Thank you.

     
