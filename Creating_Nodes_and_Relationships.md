# Creating Nodes and Relationships

Database should be blank from last section

![alt text](image-52.png)

Create a node that is Lebron James

```sql
CREATE (lebron:PLAYER:COACH:GENERAL_MANAGER {name:
"LeBron James", height: 2.01
})
RETURN lebron
```

![alt text](image-53.png)

### Create with relationships

Make Anthony Davis

```sql
CREATE (:PLAYER) - [:PLAYS_FOR {salary:34000000}] -> (:TEAM {name: "LA Lakers"})
```

![alt text](image-54.png)

Now lets look at the data

![alt text](image-55.png)

The red dot here is blank b/c it was not given the name of "Anthony Davis"

### Create relationship off of existing Nodes

Say Lebron now plays for Lakers

```sql
MATCH (lebron:PLAYER {name: "LeBron James"}), (lakers:TEAM {name: "LA Lakers"})
CREATE (lebron) - [:PLAYS_FOR {salary: 40_000_000}] -> (lakers)
```

![alt text](image-56.png)

Now we have the relationship

![alt text](image-57.png)
