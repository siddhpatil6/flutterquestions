# flutter questions


<h1> what is difference between var and dynamic in flutter ?</h1> <br>


In Flutter, var and dynamic are both used to declare variables, but they have different meanings and implications.

var is used for implicitly typed variables. When you use var, the type of the variable is inferred from the value assigned to it. Once the type is inferred, it cannot be changed. For example:

```
var name = 'John'; // The type of 'name' is inferred as String
```

dynamic, on the other hand, is used for dynamically typed variables. Variables declared with dynamic can hold values of any type, and their types can change at runtime. This is because the type checking for dynamic variables is deferred until runtime. For example:

```
dynamic value = 10; // value is an int
value = 'Hello';    // value is now a String
```

In general, it's recommended to use var when the type is clear from the initialization, and to use dynamic when you need the flexibility to change the type of the variable or when dealing with dynamic data (e.g., JSON). However, overusing dynamic can lead to less readable and maintainable code, so it's advised to use it judiciously.


<h1>  what is list in dart ? <br>
Explain following Oprations of List
Add, addAll, insert, insertAll, replaceRange, removeRange,length, reversed, first, last,isEmpty,isNotEmpty,elementAt </h1>


In Dart, a List is an ordered collection of elements. Here are the operations you mentioned:

<b>Add:</b> <br>
The add method is used to add a single element to the end of the list.

```
List<int> numbers = [1, 2, 3];
numbers.add(4);
// numbers: [1, 2, 3, 4]
```
<b>addAll:</b><br>
The addAll method is used to add all elements of another iterable (such as a list) to the end of the list.

```
List<int> numbers = [1, 2, 3];
numbers.addAll([4, 5, 6]);
// numbers: [1, 2, 3, 4, 5, 6]
```

<b>insert:</b><br>
The insert method is used to insert a single element at a specific index in the list.

```
List<int> numbers = [1, 2, 3];
numbers.insert(1, 10);
// numbers: [1, 10, 2, 3]
```
<b>insertAll:</b><br>
The insertAll method is used to insert all elements of an iterable at a specific index in the list.

```
List<int> numbers = [1, 2, 3];
numbers.insertAll(1, [4, 5]);
// numbers: [1, 4, 5, 2, 3]
```
<b>replaceRange:</b> <br>
The replaceRange method is used to replace a range of elements in the list with elements from another iterable.

```
List<int> numbers = [1, 2, 3, 4, 5];
numbers.replaceRange(1, 4, [10, 20, 30]);
// numbers: [1, 10, 20, 30, 5]
````

<b>removeRange:</b> <br>
The removeRange method is used to remove a range of elements from the list.
```
List<int> numbers = [1, 2, 3, 4, 5];
numbers.removeRange(1, 4);
// numbers: [1, 5]
```
<b>length:</b> <br>
The length property is used to get the number of elements in the list.

```
List<int> numbers = [1, 2, 3];
print(numbers.length); // Output: 3
```
<b> reversed: </b> <br>
The reversed property returns an iterable containing the elements of the list in reverse order.

```
List<int> numbers = [1, 2, 3];
var reversedNumbers = numbers.reversed;
```
<b> first: </b> <br>
The first property returns the first element of the list.

```
List<int> numbers = [1, 2, 3];
var firstNumber = numbers.first;
```
<b>last:</b><br>
The last property returns the last element of the list.

```
List<int> numbers = [1, 2, 3];
var lastNumber = numbers.last;
```
<b>isEmpty:</b><br>
The isEmpty property returns true if the list is empty, false otherwise.

```
List<int> numbers = [];
print(numbers.isEmpty); // Output: true
```
<b>isNotEmpty:</b> <br>
The isNotEmpty property returns true if the list is not empty, false otherwise.

```
List<int> numbers = [1, 2, 3];
print(numbers.isNotEmpty); // Output: true
```
<b> elementAt: </b> <br>
The elementAt method is used to access the element at a specific index in the list.

```
List<int> numbers = [1, 2, 3];
var element = numbers.elementAt(1);
// element: 2
```
These operations allow you to manipulate and access elements in a Dart list, making it a versatile data structure for storing and working with collections of data.

<h1> What is map and explain following operations of map
isNotEmpty
isEmpty
length
Keys
values
containsKeys
containsValues
remove </h1>

In Dart, a Map is a collection of key-value pairs where each key is unique. Here's an explanation of the operations you mentioned:

<b> isNotEmpty: </b> </br>
Returns true if the map is not empty (i.e., it contains at least one key-value pair); otherwise, it returns false.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.isNotEmpty); // Output: true
```

<b> isEmpty:</b> <br> 
Returns true if the map is empty (i.e., it does not contain any key-value pairs); otherwise, it returns false.
```
Map<String, int> scores = {};
print(scores.isEmpty); // Output: true
```

<b>length:</b> <br>
Returns the number of key-value pairs in the map.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.length); // Output: 2
```

<b>keys: <b> </br>
Returns an iterable containing all the keys in the map.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.keys); // Output: (Alice, Bob)
```

<b>values: <b> </br>
Returns an iterable containing all the values in the map.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.values); // Output: (100, 90)
```

<b>containsKey: <b> </br>
Returns true if the map contains the specified key; otherwise, it returns false.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.containsKey('Alice')); // Output: true
```

<b>containsValue: <b></br>
Returns true if the map contains the specified value; otherwise, it returns false.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
print(scores.containsValue(90)); // Output: true
```

<b>remove: <b> </br> </br>
Removes the entry for the specified key and returns the value associated with the key, or null if the key is not found.
```
Map<String, int> scores = {'Alice': 100, 'Bob': 90};
int removedScore = scores.remove('Alice');
print(removedScore); // Output: 100
```
These operations allow you to manipulate and access data in a Map in Dart.
