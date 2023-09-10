
<h1>MongoDB Day 1 Task</h1>
<br/>
In this Document using mongodb compass application ,
I have given the Queries that I used to get data,

The Commands which I Executed
Here the commands executed for each Questions separately:

1.Find all the information about each products<br/>
db.products.find({});<br/>

2.Find the product price which are between 400 to 800
<div>
db.products.find({product_price: { $gt: 400, $lt: 800 }});</div>
<br/>
3.Find the product price which are not between 400 to 600<br/>
db.products.find({product_price: {$not: { $gte: 400, $lte: 600 }}});
<br/>
<br/>
4.List the four product which are grater than 500 in price
<br/>
db.products.find({product_price:{$gt:500}}).limit(4)<br/>
<br/>
5.Find the product name and product material of each products
<br/>
db.products.find({},{ product_name: 1, product_material: 1 });
<br/><br/>
6.Find the product with a row id of 10<br/><br/>
db.products.find({id: '10'});
<br/>
<br/>
7.Find only the product name and product material<br/><br/>
db.products.find({},{ product_name: 1, prodduct_material: 1 });
<br/>
<br/>
8.Find all products which contain the value of soft in product material<br/><br/>
db.products.find({product_material: 'Soft'});
<br/>
<br/>
9.Find products which contain product color indigo and product price 492.00
<br/><br/>
db.products.find({$and: [{ product_price: 492 },{ product_color: 'indigo' }]});
<br/>
<br/>
10.Delete the products which product price value are same
