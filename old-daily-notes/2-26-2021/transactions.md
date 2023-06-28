# Transactions
- ACID
    - atomic, consistent, isolated, durable

- unit of work that either succeeds completely or fails
- tcl is transaction control language
- describes a group of queries that are executed as a batch that should completely succeed or have no effect at all

- A
    - atomic - all or nothing - either it succeeds or nothing happens
- C
    - consistent - -guarantees committed transaction state. No half finished transactions will occur.
    - if a transaction returns invalid data, the database reverts to a previous state that abides by the required constraints
- I
    - isolation - guarantees each transaction is individual, and other transactions don't affect one another
    - each transaction are completely separate
    - if two transactions are affecting the same data, one will have to wait
    - there are different isolation levels
- D
    - durable - a transaction isn't considered complete until it is persisted in a non volatile data storage
    - even if your device is turned off, the data is still saved

# degrees of isolation
- isolation levels define the degree to which a transaction must be isolated from the data
- if other transactions can affect your transaction, then these things can occur
    - dirty read - transaction reads uncommitted updates done by another transaction
    - non repeatable read - reads committed updates done by another transaction
        - just data row issue
    - phantom read - some rows may be added or removed due to the updates done by another transaction
        - reads same data twice, but end up getting different number of rows
        - data table issue
# isolation levels
- Read uncommitted (zero isolation)
    - does not protect transaction from anything
    - useful for when  you read and write all the time, but you're not updating data often
    - good for big picture ideas
- read committed
    - protects transaction from dirty read but not from non repeatable read
    - you can still read data from other transactions
    - locks updates unless committed
    - can only read changes if other transaction has finished committing
- repeatable read
    - locks other transactions from reading the specific row, but not for other data in the table

- serializable
    - protects transaction from phantom read - highest isolation level!
    - essentially locks the data you're working with from other transactions

    - use transactions for place order functionality - you would need to update multiple tables to actually place an order!
    - review TCL video towards the end to hear her design for product ordering
    - look over marielle's herorepo stuff!! Lots of good new notes