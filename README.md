# Useful functions for a SQL Anywhere databases

This is a collection of some useful functions that I regularly put into SQL Anywhere databases.


## Procedures

### Send_Message

- useful for outputting debug infos from other procedures
- sends a string both to the user's console (iSQL) and the server log

### RefreshMaterializedViews

Materialized views deliver their data without the need the execute the query which is more performant than a traditional query. But this comes at a price: the data *can* be stale. You have to periodically refresh the materialized views.

This procedure takes **all** materialized views in your database and refreshes them at once.  
