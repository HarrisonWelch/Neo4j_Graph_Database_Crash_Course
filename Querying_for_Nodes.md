# Querying for Nodes

Inside of Neo4j

2 types
* Nodes - entity, thing - ex: NBA player, coach team
* Relationship

Query Nodes themselves

Keyword `MATCH`
* Query for exact things

Node is represented as two parenthesis "()"

`(n)` can be used but n can be defined as anything - user alias

The `RETURN n`

So:

```
MATCH (n)
RETURN n
```

This will return all of our nodes

![Return all nodes](image-13.png)

You can download that image too

![Neo4j download](graph.png)

### Filters

What if we just want players?

Remember all nodes have labels attached to them (almost like a table name)
* Can change n to player to be more indicative of the entity type

```cypher
MATCH (player:PLAYER) RETURN player
```

![Players with filter](image-14.png)

Same with COACH objects

```cypher
MATCH (coach:COACH) RETURN coach
```

![alt text](image-15.png)

Same with Teams

```cypher
MATCH (team:TEAM) RETURN team
```

![alt text](image-16.png)

### Properties

Remember Nodes have different properties

-> We can Fetch specific properies

```cypher
MATCH (player:Player) RETURN player.name
```

![alt text](image-17.png)

This is a table now that we are dealing with lists

Can do multiple columns

```cypher
MATCH (player:PLAYER) RETURN player.name, player.height
```

![alt text](image-18.png)

### Aliasing

You can use keyword `AS` to filter different

```cypher
MATCH (player:PLAYER) RETURN player.name AS name, player.height AS height
```

![alt text](image-19.png)
