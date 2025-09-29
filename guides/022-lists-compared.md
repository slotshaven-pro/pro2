# Array-like datatypes in Python

## List [1,2,3]
Lists are the basic ordered data collection type. \
Lists can be defined with comma-separated values between square brackets [ ] \
Lists are the most general version of a sequence in Python, typically used to store collections of homogeneous items. \
Unlike strings, Lists are mutable , meaning the elements inside a list can be changed. \
Lists draw parallels with arrays in other languages. \
Lists have no fixed size. \
Lists have no fixed type constraint.

Creating lists:
```
ListEmpty = []
listOne = ['A', 1]
listTwo = list("PYTHON") # from string
listThree = list((8, 1, 2, 8)) # from tuple
listFour = list(range(11, 21)) # from range()
listFive = list([1, 3, 5, 7])
listSix = [for i in range(10)] # list comprehension
```

## Dictionary {'key':'value'}
Dictionary is a built-in compound types in Python. \
Dictionaries are ordered, mutable (= changeable), key-value pair mapping objects, typically used to store collections of data. \
As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered. \
Dictionary items can be defined within curly brackets and have a comma-separated key-value pairs. \
The values in dictionary items can be of any data type. \
Dictionaries does not allow duplicate items. \
Dictionary items are presented in key:value pairs, and can be referred to by using the key name. \
Length of the Dictionary is to determine how many items it has and can be found using built-in len() method.

Creating dictionaries:
```
numbers = {'Keyone':1, 'Keytwo':2, 'Keythree':3}

```

## Set {uniq1, uniq2}
Facts:
Set is a built-in compound types in Python. \
Sets are unordered, mutable collections of unique objects, typically used to store collections of data. \
Set items can be defined within curly brackets {} and have items with comma-separated. \
Sets does not allow duplicate values. \
Length of the set is to determine how many items a set has, using built-in len() method. \
They are defined much like lists and tuples, except they use the curly brackets of dictionaries. \
Common uses of sets include membership testing, removing duplicates from a sequence, and computing mathematical operations such as intersection, union, difference, and symmetric difference.

Creating sets:
```
setOne = {'apples', 'oranges', 'kiwi'}
setTwo = {c for c in 'abracadabra' if c not in 'abc'} # set comprehension
setThree = set(('Mon', 'Tue', 'Wed', 'Thu', 'Fri'))   # set type constructor
setFour = set([('BTC', 1), ('ETH', 2), ('ADA', 3)])   # set type constructor
setFive = set("GUIDO")
```


## Tuple (x,u)
Tuples are built-in compound types in Python. \
Tuples are ordered, immutable (= unchangeable) sequences, typically used to store collections of data. \
Tuples can be defined with comma-separated values between round brackets ( ). \
Tuples allows duplicate values. \
Tuple items are indexed, the first item has index [0] the second item has index [1] etc. \
Length of the Tuple can be found using built-in len() method.

Creating tuples:
```
tupleOne = (5,7)
tupleOne = 5,7
tupleTwo = tuple("TUPLE")   # from string
tupleThree = tuple((8, 1, 2, 8)) # from tuple
tupleFour = tuple(range(11, 21)) # from range()
tupleFive = tuple([1, 3, 5, 7])  # from list
stockPrices = (('AAPL', 135.73), ('TSLA', 130.92), ('MSFT', 238.65)) # tuple of tuples
```
