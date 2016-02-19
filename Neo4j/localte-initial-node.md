How does Neo4j locates the initial node?
---

Neo4j is highly optimized for traversing property graphs. Under ideal circumstances, it can traverse millions of nodes and relationships per second, following chains of pointers in the computer’s memory.

However, before traversal can begin, Neo4j must know one or more starting nodes. Unless the user (or, more likely, a client program) can provide this information, Neo4j will have to search for these nodes.

> A “brute force” search of the database (eg, for a specified property value) can be very time consuming. Every node must be examined, first to see if it has the property, then to see if the value meets the desired criteria. To avoid this effort, Neo4j creates and uses indexes. So, Neo4j uses a separate index for each label/property combination.

To create an index, use the following command:

`CREATE INDEX ON :Label(propertyName);`

For eg., `CREATE INDEX ON :Movie(title);`
