# Collections
- A collection is a data structure that can hold one or more items.
- All collections provide methods to add, remove, and find data
- System.Collections is the namespace

- all collections under the ICollection interface can enumerate, copy to array, show capacity an dcount properties, and has a consistent lower bound (0).
- The IEnumerable interface provides a way to move through the collection

# Arrays
- A collection of objects of the same data type stored in a contiguous space
- There are single dimensional, multidimensional and jagged arrays
    - Jagged arrays are arrays of arrays
- Array sizes are immutable! Once an array is instantiated, you cannot change it's size.

# Non Generic Collections
- Used to store data when the size is unknown. This makes sure you only take up the memory needed!
- Common non generic collections
    - Arraylist
    - Hashtable
    - Stack
    - Queue
- Generic collections store data as objects - what if we store objects of different types in the same collection?
    - We should enforce type checking before storing in a non generic collection (I think this is the <> brackets)


# generic collections
- These are safe collections because you enforce a data type.
- At runtime you have to make sure to set the type.
- List<T>
    - List of objects that can be accessed by index
    - ever expanding array
- Dictionary<T>
    - key/value pairs that are organized based on the key
    - this is a tuple because it needs a key and a value
- Stack<T>
    - LIFO
    - a stack of plates you take from the top!
- Queue<T>
    - FIFO
    - Like any normal line, like a line for concert tickets.


