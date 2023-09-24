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

##
##
##
##
##
##
##
##
