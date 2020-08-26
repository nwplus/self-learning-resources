# Types of Databases

Now that you know what a database is and why you need one, how do you go about choosing one? There are many different databases for each need but we will focus on the two main categories, relational and non-relational.

## Relational Databases

### Structure

Relational databases are table-based, you can think of them kind of like a more powerful excel spreadsheet! They are called relational because you can define relationships between different tables. For example, each customer could have an id and each order would have the id of the customer who it belonged to:

![Example of database relations](/images/db-relations.png)

For relational databases, the schema must be predefined, which provides a rigid structure where you can specify constraints. For example, you could ensure that a column like order amount must be positive doubles only, which can help to keep data consistent.

They also tend to follow the ACID model, which is super important for data validity:

* **A**tomicity: All the changes are performed or none of them are. This prevents partial updates to the database, which can cause greater problems than just rejecting the whole transaction.
* **C**onsistency: Changes must lead to a valid state, maintaining database invariants or rules. This prevents database corruption by an illegal transaction.
* **I**solation: Ensures that if the changes were done concurrently, you would get the same result as doing them sequentially.
* **D**urability: After a transaction successfully completes, changes to data persist and are not undone, even in the event of a system failure (e.g., power outage or crash).

### Language

Most relational databases use the same structured query language (SQL) for defining and manipulating data. SQL follows the declarative programming paradigm, which means you describe **what** needs to be done, not **how** to get it done. In turn, this allows for more complex queries on data.

### Scalability

In general, relational databases are vertically scalable. This means that you scale by adding more power to one machine (CPU, RAM, SSD).

### Downsides

SQL can be restrictive in the sense that it requires that you use predefined schemas to determine the structure of your data before you work with it. This can require significant up-front preparation, and it can mean that a change in the structure would be both difficult and disruptive to your whole system. Additionally, with the increasing prevalence of cloud computing, not being horizontally scalable can be seen as a downside since you can only increase the power of one machine so much.
