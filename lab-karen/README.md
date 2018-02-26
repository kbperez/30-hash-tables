## Lab 30-hash-table
Creating and testing a hash table data structure implementation with a hashTable constructor, a hashKey method, a set method to insert nodes, a get method to retrieve nodes/data and a remove method to delete nodes.  Data storage in each hashTable bucket/array is implemented with a singly linked list.

### Installing

Fork this repo and install on your local machine using git clone.
Type *npm i* to install required dependencies - jest for testing and eslint.

You may type your code in index.js to generate hashTables and use methods. Type *node index.js* to run in Node.js repl.

Type *npm run test* to run tests.

###  Using data structures and accessing each method

You may type your code in index.js to generate hashTables and use methods. Type *node index.js* to run in Node.js repl.

**To create a hash table of size n**
```
let hashTable = new HashTable(n);
```

**To set values in a hash table, enter key and value as strings**
```
hashTable.set('address', 'content');
```
This will set an object in the hash table array matching the hashkey.  In this case, the hashKey has a value of 2.

```
[ undefined,
  SLL { head: Nd { key: 'address', value: 'content', next: null } },
  SLL { head: Nd { key: 'yek', value: 'value', next: null } } ]
```

**To get data from a hash table, enter a key - as a string**
```
hashTable.get('address');
```
This will return a node.
```
Nd { key: 'key', value: 'value', next: null }
```

**To remove data from a hash table, enter the key - as a string**

```
hashTable.remove('address');
```

This will an empty SLL.

```
[ undefined,
  SLL {},
  SLL { head: Nd { key: 'yek', value: 'value', next: null } } ]
```

### Testing
Tests are included for:
- hashTable constructor = hash-table-constructor.test.js
- hashKey method = hash-table-hashKey.test.js
- set method = hash-table-set.test.js
- get method = hash-table-get.test.js
- remove method = hash-table-remove.test.js

Documentation
in your README, write documentation for you data structures
your documentation should includes code block usage examples
provide instructions for:
installing and using your data structure
accessing each method
running your tests
Feature Tasks
create a HashTable constructor
the buckets should be implemented as an array of Singly Linked Lists
implement the following prototype methods
.hash(key) converts a string into a number that will index your buckets
`.set(key, value) stores a value in the hashed keys bucket
`.get(key) looks in the hashed keys bucket and returns the value of the node containing the key, or null if not found
`.remove(key) removes the dll node node containing the key