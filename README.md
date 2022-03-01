# Just Tech News

* Drops tables if changes are made
making Sequelize create new tables if the data model or model associations have changed by using the command `sequelize.sync({force:true})` in the `server.js` file

* IMPORTANT!!! Make sure this PUT route is defined before the `/:id` PUT route, though. Otherwise, Express.js will think the word "upvote" is a valid parameter for `/:id`.


## Tools
`JawsDB` Add-On (Links to an external site.) is a Heroku add-on that provides a fully functional MySQL database server for use with your Heroku application.

`Sequelize` (Links to an external site.) is a Promise-based Node.js ORM for Postgres, MySQL, MariaDB, SQLite, and Microsoft SQL Server. It features solid transaction support, relations, eager and lazy loading, and read replication. You’ll use the Sequelize package (Links to an external site.) to add Sequelize to your Node.js applications. 
(Sequelize is a tool for object-relational mapping (Links to an external site.), or ORM. This means that it sits between the server's API endpoints and the SQL database to translate and normalize data between JavaScript and SQL. We'll write JavaScript to model the database structure, and Sequelize will handle all of the SQL queries.)
(With Sequelize, we no longer have to bother with creating the entire SQL table schema and running it through the SQL shell. All we need to do is create a database; then when we start the app, Sequelize will create the tables for us!)

`mysql2` Sequelize prefers to work with the mysql2 library, which appears to be the successor of the native mysql library for Node.js.


`Dotenv` (Links to an external site.) is a zero-dependency Node.js module that loads environment variables from a .env file into process.env, a Node.js property that returns an object containing the user environment. This allows developers to store user environment configuration—or the things that are likely to vary between different deployments (passwords, secrets, keys, etc.)—separately from their code.

`bcrypt` (Links to an external site.) is a Node.js library that allows you to hash passwords. Hashing is the process of taking input and using a mathematical formula to chop and mix it up to produce an output of a specific length. Hashing is a one-way function, meaning that it can easily convert input to a fixed-size output, but it is difficult to invert, or convert in the opposite direction. This attribute allows developers to secure passwords when authenticating users for their applications.

## Learning
Set up the application to use Sequelize to manage SQL data.

Use environment variables to protect sensitive data.

Create a user table using Sequelize models.

Create all of the server endpoints using RESTful API standards to work with the `User` model’s data.
* (Nice work setting up your first Express.js API using Sequelize! We created a data model for the user and built the server endpoints using RESTful APIs. The User data model enables the application to create and manipulate user data. Now users can maintain authorship of their posts, comments, and votes by logging into the website with their personal credentials, such as email and password.)

Secure user passwords stored in a database with hashing.

Add Sequelize hooks (lifecycle events) at key junctures in the application workflow to process important tasks

Use `async` and `await` keywords to handle asynchronous functionality to increase legibility.

Create user authentication that enables identity verification with a hashed password.

Make associations to reflect relationships between models.

Use `include` to JOIN associated table data in queries.

Create API endpoints to execute CRUD on a Post.

Create a new Vote model to store data about who is voting on which posts.

Implement a many-to-many model association using Sequelize.

Create a route allowing a user to vote on a post.

Update existing routes to query for related data to see who has voted on what post.

Clean up some of the code with a custom static Sequelize model method.





## Steps
Model the data.

Set up API routes to work with that data.

Test the routes to make sure everything works as intended.

Repeat with new model.

Incorporate a password hashing algorithm package to encode stored user passwords.

Intervene during the create and update operations using hooks in the model.

Use instance methods to compare user passwords in the login process.

Create a login route for authentication.

Create the `Post` model. Define the Post data model to declare the columns, data types, and validation.
Define model associations. Declare the model’s relationships and the foreign key references.
Create API routes for the Post model. Use RESTful APIs to allow the resources for the database to be accessible.

Create the Vote model. We’ll create the Vote model that will hold data connecting the User and Post models and create the relationship between them.
Create PUT route for voting on a post. We’ll create a route that updates a post by adding a vote to it.
Update GET routes to include votes. We’ll edit some of the queries to include data for related votes.
Refactor messy code. Some of the routes may look a little busy after adding this new code, so let’s use a Sequelize feature to clean it up. (Before we can create or update any routes to include vote data, we need to create the Vote model to hold data connecting the User and Post models. Once we’ve created this model, we should first create a route to update a post by adding a vote to it. Then we can update the GET routes to return the vote data. Finally, we’ll use a Sequelize feature to clean up the code.)