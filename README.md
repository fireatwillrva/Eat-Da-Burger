# Eat Da Burger!
A Burger Eatin' Application with Node.js/Express/MySQL/Handlebars/Materialize

## Description

*Eat Da Burger* is a simple full stack burger menu application. The user may enter any burger name to add it to the menu. Doing so will place the burger in the *available* menu in green on the left side of the screen. This also adds the new burger entry into the MySQL database. The user may then eat any burger by clicking on it, which moves it into the the adjacent column and updates its status accordingly in the database.

The application is implemented using a [Node.js](https://nodejs.org/en/) and [Express](https://expressjs.com/) server on the back end, a [MySQL](https://www.mysql.com/) database and [Handlebars](https://www.npmjs.com/package/handlebars) with [Materialize](https://materializecss.com/) on the front end.

## Demo

The demo of the burger eating application can be found [here](https://afternoon-mesa-92069.herokuapp.com/) on Heroku.

### Installation

To install the application follow the instructions below:

``` Javascript
	git clone git@github.com:fireatwillrva/Eat-Da-Burger.git
	cd Eat-Da-Burger
	npm install
```

### MySQL Database Setup

In order to run this application, you should have the MySQL database already set up on your machine. If you don't, visit the [MySQL installation page](https://dev.mysql.com/doc/refman/5.6/en/installing.html) to install the version you need for your operating system. Once you have MySQL isntalled, import the database with the SQL code found in [schema.sql](./db/schema.sql) in the *db* folder. You can populate the table by then importing [seeds.sql](./db/seeds.sql) or by adding them in the application.

### Interface Setup

In order to get your menu online, you'll need to connect to a port in [MAMP](https://www.mamp.info/en/). Click on the **Start Servers** button in MAMP then click the **Open WebStart page** button. Your port information will be listed on the left side under *My SQL*. Take that information and replace the connection parameters on line 13 of [connection.js](./config/connection.js) (as shown below) in the *config* folder with your port info.

``` Javascript
	host: 'localhost',
	port: 8889,
	user: 'root',
	password: 'root',
```
	
### Running Locally

To run the application locally and access it in your browser, open [server.js](./server.js) in the terminal and run the command below.

``` Javascript
	node server.js
```
	
The application will now be running locally in your browser at the URL `http://localhost:8080`. *Enjoy!*
