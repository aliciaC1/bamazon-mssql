# bamazon-mssql
Amazon-Like storefront web application using MS-SQL. The app will take orders from customers and deplete stock from store's inventory. 
This application implements a simple command line based storefront using the npm inquirer package and the MS-SQL database backend together with the npm mssql package. The application presents two interfaces: customer and manager.

## MS-SQL Database Setup
In order to run this application, you should have the MS-SQL database already set up on your machine. If you don't, visit the MS-SQL installation page to install the version you need for your operating system. Once you have MS-SQL isntalled, you will be able to create the Bamazon database and the products table with the SQL code found in `bamazon.sql`. Run this code inside your MS-SQL client to populate the database, then you will be ready to proceed with running the Bamazon customer and manager interfaces.

## Customer Interface
The customer interface allows the user to view the current inventory of store items: item IDs, descriptions, department in which the item is located and price. 

![alt text](./imgs/demo.gif)

The user is then able to purchase one of the existing items by entering the item ID and the desired quantity. If the selected quantity is currently in stock, the user's order is fulfilled, displaying the total purchase price and updating the store database.

![alt text](./imgs/buy2.gif)
![alt text](./imgs/buy1.gif)

If the desired quantity is not available, the user is prompted to modify their order.

![alt text](./imgs/error1.gif)

To run the customer interface please follow the steps below:

'git clone' 
'cd bamazon'
'npm install'
'node bamazonCustomer.js'

## Manager Interace
The manager interface presents a list of four options, as below.

The View Products for Sale option allows the user to view the current inventory of store items: item IDs, descriptions, department in which the item is located, price, and the quantity available in stock.

![alt text](./imgs/viewprod.gif)

The View Low Inventory option shows the user the items which currently have fewer than 100 units available.

![alt text](./imgs/lowin.gif)

The Add to Inventory option allows the user to select a given item ID and add additional inventory to the target item.

![alt text](./imgs/addinv.gif)

The Add New Product option allows the user to enter details about a new product which will be entered into the database upon completion of the form.

![alt text](./imgs/newprod.gif)

To run the manager interface please follow the steps below:

'git clone'
'cd bamazon'
'npm install'
'node bamazonManager.js'

## NPM Packages
-mssql 
-inquirer
-figlet
-tty-table
-chalk
-node-emoji