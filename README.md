# ORM
    ORM stands for Object Relational Mapper. Here Object refers to: Obejct Oriented Programming,
    Relational refers to: Relational Database( Like mysql) and Mapper refers to: Mapping of relational
    db syntax to an Object oriented syntax

    ORM acts as a layer between the developer and the databases, and it helps us to visualise and 
    even code all the relation logic in the form of object oriented code. That means, every entity
    which becomes a table in relational database, can be treated as a blue print, and the entries of
    the tables can be treated as new object. So it establishes a relation between tables and objects.

    This concept is not only limited to NodeJs or Mysql, but other big frameworks like Ruby on Rails,
    Django etc by default support ORM. for our usecase i.e. for NodeJs we need to use a Third part
    ORM which is Sequalize.


    So in Order to setup a basic demo project
``` 
    npm init
    npm i express
    npm i sequelize mysql2
    npm i sequelize-cli

```

    Express: to setup basic server
    mysql2: to get dependent packages required to connect to a mysql db
    Sequelize: this is the actual sequalize package we are going to use to get functionality of the ORM
    Sequelize-cli: this is going to proveide few command line tools to work with sequelize ORM



## How we connect to mysql Databse?

    So the mysql databse actually runs on a mysql server. and just like any server it will be
    responsible for handling request coming to it. So also has a port number associated a url etc,
    but because of Sequalize ORM we don't need to bother about the port number and url etc,
    Sequalize provides a very simple way for connecting to the mysql server.


    EXPRESS SERVER-------> MYSQL SERVER and this connection and request cycle will be
    handled automatically by our ORM.

## Schema

    Schema is the blue print of your relational databse. Example: we define that we will have one
    table named student, with 3 columns, name as varchar, age as int, marks as int.

    Schema migration refers to any change to the schema being recorded.

    whenever we change something in the schema it acts as a new migration.

## Development, Test and Production Db

    Development databse will be your local database, residing in your own computer, so every 
    developer will be having their own local development database.

    Test db is setup for testing new features that we are going to release, and that is generally
    common for all developers.

    prodeuction db is the actual live database that your application interacts with when users do some
    action on the application.


## Setting up Sequelize

    So in order to setup basic sequelize we can manually create configuration and folders, but it 
    automatically provides a CLI interface in order to get things done easily.

    ```
        npx sequelize init
    
        this command will initialize basic folders and configuration
    ```

    then inside config/config.json file we have our code that will actually connect to the
    mysql server. in that code all we have to do is just change the name database, whatever we want
    to keep and the username and password of our mysql server we need to feed.

    As soon as we are done with the changes run the following command.

         npx sequelize db:create

         this will actually create a new database in mysql

##  Creating Tables

    So in order to create tables we can use the following command
    ```
        npx sequelize model:generate --name student --attribute name:string, age:integer
    ```

    here the name is mentioning the name of the table and the -attribute are mentioning the column
    and the types of the command of the tables.

    The moment we execute this command we get a model file, and a migration file. migration file
    contains the actual code that sequelize executes for creating the table, if we want to make some
    changes in the schema, we can change the migration file. once we are sure about the change 

    we can execute
        ```
            npx sequelize db:migrate
        ```




##
##
##
##
##
