# Lab 2. Creating app that uses database. PostgreSQL
Website devoted to selling clothes.

## Graphical ER Model(Chen notation)
![ERD](/lab2/erd.jpg)

## Database relations and tables
![Relations](/lab2/relations.jpg)

## Data description
Relation | Attribute | Data type
------------ | ------------- | -------------
buyer | `id` - unique attribute of every user, primary key <br>`name` - name of the user <br>`email` - email of the buyer <br>`hashed_password` - password of the buyer saved in hash form<br>`city` - city of the buyer <br>`postal_code` - postal code of the buyer| bigint<br>text<br>text<br>text<br>text<br>text
product | `id` - unique attribute of the product <br>`name` - name of clothes <br>`description` - description of clothes, its color, sizes available and charasteristics  <br>`price` - asking price of the product <br>`total_quantity` - total quantity of the product | bigint<br>text<br>text<br>numeric<br>bigint
order |`id` - unique attribute of every order <br>`date` - cut-off date when an order is closed <br>`buyer_id` - id of the buyer, who placed the order | bigint<br>date<br>bigint
order_item |`id` - unique attribute of the order item <br>`order_id` - id of the order, to which this item belongs <br>`product_id` - id of the product, which lays in this order item <br>`amount` -  the total number or quantity of the product | bigint<br>bigint<br>bigint<br>bigint
