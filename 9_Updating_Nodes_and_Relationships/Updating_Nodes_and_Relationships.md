# Updating Nodes and Relationships

We want to add the name of Anthony Davis because we forgot it.
* Query using an id

```sql
MATCH (anthony: PLAYER) 
WHERE ID(anthony) = 0
RETURN anthony
```

![alt text](image-58.png)

### Use `SET`

```sql
MATCH (anthony: PLAYER) 
WHERE ID(anthony) = 0
SET anthony.name = "Anthony Davis"
RETURN anthony
```

![alt text](image-59.png)

## Change and Add props

```sql
MATCH (lebron: PLAYER) 
WHERE ID(lebron) = 3
SET lebron.height = 2.02, lebron.age = 36
RETURN lebron
```

![alt text](image-60.png)

### Adding labels

```
MATCH (lebron: PLAYER) 
WHERE ID(lebron) = 3
SET lebron:REF
RETURN lebron
```

He now has 4 different labels

![alt text](image-61.png)

### Updating relationships

Update the salary to be a little larger

```sql
MATCH (lebron {name: "LeBron James"}) - [contract: PLAYS_FOR] -> (team: TEAM)
SET contract.salary = 60_000_000
RETURN lebron, team
```

![alt text](image-62.png)

### Removing props

Remove the REF label and the age prop from LeBron

```sql
MATCH (lebron: {name: "LeBron James"})
REMOVE lebron.age
```

![alt text](image-63.png)

Same with labels

```sql
MATCH (lebron {name: "LeBron James"})
REMOVE lebron:REF
RETURN lebron
```

![alt text](image-64.png)
