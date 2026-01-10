## How it works:

From within the terminal run:
- python -m venv env
- source env/bin/activate
- pip install -r requirements.txt
- python3 app.py
  
# to run the flask rest api
- python3 flask_rest_api.py

Console application that loads an existing store's inventory data from a CSV file into a SQLite database. 
The application will allow a user to interact with the records stored in the database to view existing records, add new items, and backup/export the existing state of the database into a CSV file.

Uses CSV and File I/O and database ORMs to build a console application that allows to easily interact with data for a store's inventory. 
The data needs to be cleaned from the CSV before it is added to the database. 
All interactions with the records should use ORM methods for viewing records, creating records, and exporting a new CSV backup.
CRUD operations

Creates a model called Product that the SQLAlchemy ORM will use to build the database. 
The Product model should has five attributes: product_id, product_name, product_quantity, product_price, and date_updated.
Uses SQLALchemy’s built-in primary_key functionality for the product_id field, so that each product will have an automatically generated unique identifier.


Connects the database and creates tables
Within the dunder main method:
connected to the database created/initialized
load the CSV products data into the created table
Run the application so the user can make menu choices and interact with the application.

Read the existing CSV file
Read the inventory.csv file, and create a list that contains each product inside the csv file as a dictionary. 
Cleaning up the data before adding each product dictionary to a list:
product_id will be stored as SQLAlchemy’s built in primary_key
product_quantity will be stored as an integer
product_price will be stored as an integer and converted to cents ($3.19 becomes 319, for example)
date_updated will be stored as a Date object.

Add the data from CSV into the database
Function that will add the products listed in the inventory.csv file to the database.

Creates a Menu to make selections
Function to handle interaction with the user of your app. 
prompt the user to enter v in order to view the details of a single product in the database, a to add a new product to the database, or b to make a backup of the entire contents of the database.

Displaying a product by its ID - Menu Option V
function to handle getting and displaying a product by its product_id.

Adding a new product to the database - Menu Option A
function to handle adding a new product to the database. 
prompt the user to enter the product's name, quantity, and price. process the user-provided value for price from a string to an int. the value stored for the price field to the database is converted to cents ($2.99 becomes 299, for example).

Backup the database (Export new CSV) - Menu Option B
function to handle making a backup of the database. The backup is written to a .csv file.



-----

####

## Features:

SQLAlchemy script to make a db file in SQLite with an instance of a model class. import a csv file
the script will run backups of the database in SQLite format

The second script is to build an API with Flask framework

-----

#####

## Technologies Used:

- Python
- SQLAlchemy
- SQLite
- CSV module

-----

#####

## Skills Learned:

- relational databases
- csv
- ORM

-----

###

Clone the repo:

```bash
git clone https://github.com/gutiluis/Techdegree-project-4.git
```
