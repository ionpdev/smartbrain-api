# SmartBrain-api - v1
Project developed during my Udemy course certification

1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. You must add your own API key in the `controllers/image.js` file to connect to Clarifai API.

You can grab Clarifai API key [here](https://www.clarifai.com/)

** Make sure you use postgreSQL instead of mySQL for this code base.

The DB:

login table:
CREATE TABLE login (
id serial PRIMARY KEY,
hash varchar(100) NOT NULL,
email text UNIQUE NOT NULL
);

users table:
CREATE TABLE users (
id serial PRIMARY KEY,
name VARCHAR(100),
email text UNIQUE NOT NULL,
entries BIGINT DEFAULT 0,
joined TIMESTAMP NOT NULL
);