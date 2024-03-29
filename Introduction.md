
https://www.youtube.com/watch?v=8jNPelugC2s

Neo4j

Graph database

Database is somewhere where application data is stored

For example - Twitter.
* Need a placed to store accounts, pictures, text

Of Course we need a DB
* Store DB
* Retrieve Data
* Update Data
* Delete Data

10,000 diff types DB

SQL
* Tables
* Strict schemas
* Use for strictness - sensitive data

Document DBs
* Mongo
* Schemaless

Redis
* Key Value pair DBs
* Allow fast retreival

SQL DBs

Twitter
* Tweet and a user liked it
* relationship of a LIKE between a user and a tweet

Sometimes the relationships are so cumbersome that we need a DB to focus on the links

=> This is what Neo4j is going to do

### Inside Graph DBs

Graph DBs store records in "Nodes"

In a node we can store any "thing"
* Laptop
* Person
* Tweet
* etc

Example
* NBA Player - LeBron

If we want multiple Basketball players you can also have them in the DB as Nodes

Store different things

Teams - Lakers and Nets

LeBron has the relationship "PLAYS_FOR" Lakers
* Russell Westbrook has this
* Anthony Davis has this

Kevin and James play for the Brooklyn Nets

LeBron is a TEAMMATE to Russell
* Another TEAMMATE relationship from Russ to LeBron
* An similar sets of teammates

### Back to LeBron

We have LeBron
* Each node can properties
  * name: LeBron
  * weight: 120
  * height: 2.2

Lakers node would be
* name: LA Lakers

Give each node a label
* Player
  * Name
* Team
  * Name

Relationship
* Always in 1 direction

PLAYS_FOR
* Can also add properties
* salary: 40M
* Can simply query (all) the PLAYS_FOR relationship(s) LeBron has
