# ecommerce-backend-assessment  

# Django Assessment Task 

## Assessment Parameters: 
1. Response Format 
2. Edge Cases Handling  

## The Task: 

## Overview: 
You are backend engineer for a upcoming ecommerce website MVP. Your backend should be able to keep track of catalogue of various items and do CRUD operations on them. 

Your Database Schema should look something like this: 

|  Row Name |  Datatype  |
| ------------ | ------------ |
| ID   | Integer   |
| Name_of_Item  |  String  |
|  Item_Category  |  String  |
|  Delivery Time   |  Integer  |
|  Rating | Float | 
| Warehouse_Stock | Integer |
| Price | Integer | 
| Created_Timestamp | Datetime |     
| Sales_count | Integer


You should have the following APIs: 

#### 1. /list_items   
This API will be used to list items for customer UI. Thus only necessary items should be returned here. You need to send the following values in this api: 
a. Name 
b. Item Category 
c. Delivery Days 
d. Rating  
e.  Price 

This API should have the following filters: 
1. filter by name (using substring and not absolute string matching)
2. get items with more than 'n' ratings, 'n' will be passed in the API as query parameter. Suppose 'n' is 3, then API should fetch all items with rating >=3
3. Delivery Days less than 'n'  (similar to rating but in opposite way)
4.  Sort by ascending / descending based on price.  The API will have 'sort_type' which can have 'asc' or 'dsc' to determine type of sorting.  

#### 2. /get_item_data   
This API is to get detailed data for each item. Return everything related to a item. Use item_id or id as reference. 

#### 3. /buy_item  
This API will take id of item. It will update 2 things : 
a. Increase Sales Count by 1 
b. Decrease Warehouse_Stock by 1   

Bonus: 
1. Return an error if Warehouse_Stock is 0

#### 4. delete_item 
This API will delete an item based on id.  

#### 5. Add product 
Add a product to the catalogue

#### 6. rate_product  (Bonus)
This API will take item_id and rating and then update the rating using the following formula: 

updated_rating = ((sales * current_rating) + input_rating ) / (sales + 1)


#### More Bonus: 
1. 2 products can't have the same name 
2. Increase the price of product once sales go above 100 units  
3. Automate the creation of products using some CSV stuff. 

#### Submission Guidelines 
1. Attach postman collection of your APIs so it's easy to test. Place the postman collection in a seperate folder 'postman'
2. Write a readme whichi instructs how to run the program    
3. Use SQLite DB so that you can share the database with us on the repo itself.
4. Create a branch of your name and push the code there 
5. When your assignment is finished, create a commit "ready for testing" and tag that commit as '1.0.0'. How to tag a commit - https://devconnected.com/how-to-create-git-tags/   
6. Don't forget to push that tag! 
7. Write good and awesome code 


### Note: 
1. Do error handling well, there should be ** No error pages** . Try to handle each case with a message like : "Sorry the item_id doesnt exist' or "Sorry, the item is out of stock".  
2. Return Status Code as well 
3. Initialize Database with static values as necessary. You can either use a csv to feed data or use a DB software as you deem fit.  
4. Attach Postman collection in the repo.  
5. Bonus **cannot** compensate for basic functionalities. Focus on the basic functions first.  


#### Reference Material: 
1. The internet 
2. The documentation - https://docs.djangoproject.com/en/4.1/topics/db/queries/   

## All the Best! 

## Happy Coding!
