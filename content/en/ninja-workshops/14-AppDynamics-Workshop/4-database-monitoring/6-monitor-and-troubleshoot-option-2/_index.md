---
title: Monitor and Troubleshoot - Part 2
time: 2 minutes
weight: 5
description: In this exercise you will review the queries dashboard, review the details of an expensive query, and troubleshoot an expensive query.
---

## Review the Queries Dashboard

The Queries window displays the SQL statements and stored procedures that consume the most time in the database. You can compare the query weights to other metrics such as SQL wait times to determine SQL that requires tuning.

1. Queries tab: Displays the queries window.
2. Top Queries dropdown: Displays the top 5, 10, 100 or 200 queries.
3. Filter by Wait States: Enables you to choose wait states to filter the Query list.
4. Group Similar: Groups together queries with the same syntax.
5. Click on the query that shows the largest Weight (%) used.
6. View Query Details: Drills into the query details.

You can read more about the Database Queries dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/database-visibility/monitor-databases-and-database-servers/monitor-database-performance/database-queries-window)

![Queries Dashboard](images/07-db-dashboard-01.png)

## Review the details of an expensive query

Once you have identified the statements on the Database Queries window that are spending the most amount of time in the database, you can dig down deeper for details that can help you tune those SQL statements. The database instance Query Details window displays details about the query selected on the Database Queries window.

1. Resource consumption over time: Displays the amount of time the query spent in the database using resources, the number of executions, and the amount of CPU time consumed.
2. Wait states: The activities that contribute to the time it takes the database to service the selected SQL statement. The wait states consuming the most time may point to performance bottlenecks.
3. Components Executing Similar Queries: Displays the Nodes that execute queries similar to this query.
4. Business Transactions Executing Similar Queries: Displays the Java business transactions that execute queries similar to this query.

![Expensive Query Details](images/07-db-dashboard-02.png)

1. Use the outer scroll bar on the right to scroll down.
2. Clients: Displays the machines that executed the selected SQL statement and the percentage of the total time required to execute the statement performed by each machine.
3. Query Active in Database: Displays the schemas that have been accessed by this SQL.
4. Users: Displays the users that executed this query.
5. Query Hashcode: Displays the unique ID for the query that allows the database server to more quickly locate this SQL statement in the cache.
6. Query: Displays the entire syntax of the selected SQL statement. You can click the pencil icon in the top right corner of the Query card to edit the query name so that it is easy to identify.
7. Execution Plan: Displays the the query execution plan window.

You can read more about the Database Query Details dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/database-visibility/monitor-databases-and-database-servers/monitor-database-performance/database-queries-window/database-query-details-window)

![Expensive Query Details](images/07-db-dashboard-03.png)

## Troubleshoot an expensive query

The Database Query Execution Plan window can help you to determine the most efficient execution plan for your queries. Once you’ve discovered a potentially problematic query, you can run the EXPLAIN PLAN statement to check the execution plan that the database created.

A query’s execution plan reveals whether the query is optimizing its use of indexes and executing efficiently. This information is useful for troubleshooting queries that are executing slowly.

1. Notice that the join type in the Type column is ALL for each table.
2. Hover over one of the join types to see the description for the join type.
3. Examine the entries in the Extra column.
4. Hover over each of the entries to see the description for the entry.

The descriptions in the Explain Plan Details point to the use of full table scans across all three tables in the query.

Let’s investigate the indexes on the table using the Obect Browser next.

5. Click on the Object Browser option to view details of the schema for the tables

You can read more about the Database Query Execution Plan dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/database-visibility/monitor-databases-and-database-servers/monitor-database-performance/database-queries-window/database-query-execution-plan-window)

![Troubleshoot Expensive Query](images/07-db-dashboard-04.png)

1. Choose the Database option.
2. Click on the supercars schema to expand the list of tables.
3. Click on the CARS table to see the details of the table.
4. You can see that the CAR_ID column is defined as the primary key

![Troubleshoot Expensive Query](images/07-db-dashboard-05.png)

1. Use the outer scroll bar to scroll down the page.
2. Notice the primary key index defined in the table.
3. Click on the MANUFACTURER table to view its details.

![Troubleshoot Expensive Query](images/07-db-dashboard-06.png)

1. Notice the MANUFACTURER_ID column is not defined as a primary key.
2. Scroll down the page to see there are no indexes defined for the table.

The expensive query you looked at is joining across three tables and could benefit from an index for each column in each join. The MANUFACTURER_ID column needs an index created for it to improve the performance of any queries on the table.

![Troubleshoot Expensive Query](images/07-db-dashboard-07.png)

You have now completed this lab!

Next we’ll start the Business iQ lab.