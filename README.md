# SQL query logic implementation
## Iterator Model and Operator Implementation

Implemented operators in the open(), next(), close() iterator model (e.g., via an
iterator base class and derived operators classes) in Python. 
* TblScan(filename): A table scan operator that takes a string filename of a csv file, and
returns its rows (each as an array of strings) in the sequence they appear in the file.
* EqSelect(input, attr, value): A selection operator that takes an iterator input (i.e.,
a sub query), an attribute position attr, an integer value, and returns only rows t where
t[attr] == value.
* HashJoin(input1, input2, attr1, attr2): A join operator that takes two iterators
input1 and input2, as well as attribute positions attr1 and attr2, and performs a hash
join with condition t1[attr1] == t2[attr2] (expecting input2[attr2] to be unique).
* HashCountAgg(input, attr1, attr2): A group-by operator that takes an iterator input,
as well as attribute positions attr1 and attr2, and performs a hash group-by with grouping attribute attr1, aggregate attribute attr2
