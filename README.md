 ## Pizza Challenge A

This is a  application for a pizza restaurant that allows you to manage restaurants, pizzas, and the association between them.

---------------

1. Clone the repository:
```bash
git clone https://github.com/JamesLawwd/challenge-pizza-code.git
```
2. Create a virtual environment:


3. Install the required packages:
```
pipenv install
```
4. Initialize the database:
```bash
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```
5. Run the application:
```
flask run
```
6. Access the application at `http://localhost:5555` in your web browser.

API Documentation
----------------

### Restaurants

#### Get all restaurants

`GET /restaurants`

#### Get a restaurant by ID

`GET /restaurants/<int:restaurant_id>`

#### Create a new restaurant

`POST /restaurants`

#### Update a restaurant

`PUT /restaurants/<int:restaurant_id>`

#### Delete a restaurant

`DELETE /restaurants/<int:restaurant_id>`

### Pizzas

#### Get all pizzas

`GET /pizzas`

#### Get a pizza by ID

`GET /pizzas/<int:pizza_id>`

#### Create a new pizza

`POST /pizzas`

#### Update a pizza

`PUT /pizzas/<int:pizza_id>`

#### Delete a pizza

`DELETE /pizzas/<int:pizza_id>`

### Restaurant-Pizza Associations

#### Get all associations

`GET /associations`

#### Get an association by ID

`GET /associations/<int:association_id>`

#### Create a new association

`POST /associations`

#### Update an association

`PUT /associations/<int:association_id>`

#### Delete an association

`DELETE /associations/<int:association_id>`


```
## Database Schema


The database schema consists of three tables: `restaurants`, `pizzas`, and `associations`. The `restaurants` table contains information about each restaurant, the `pizzas` table contains information about each pizza, and the `associations` table contains information about the association between a restaurant and a pizza, including the price of the pizza at that restaurant.

The `restaurants` and `pizzas` tables are related through the `associations` table, which has foreign keys to both the `restaurants` and `pizzas` tables.

The database schema is defined in the `models.py` file.

Seed Data
---------

Seed data is provided in the `seed.py` file. To populate the database with seed data, execute the following command:
```
python seed.py
```

License
-------

This project is licensed under the MIT License.


## Author
James