a method used to keep a database connection open.

## why

many reasons:

- creating a new database connection is expensive
   - open network session
   - authenticate
   - check authorization
- database not allowing more than certain amount of connection
- need to use in serverless functions
  ... and so on.
