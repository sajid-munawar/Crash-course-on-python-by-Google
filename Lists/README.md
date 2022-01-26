## Lists and Tuples Operations Cheat Sheet
#### Lists and Tuples Operations Cheat Sheet
Lists and tuples are both sequences, so they share a number of sequence operations. But, because lists are mutable, there are also a number of methods specific just to lists. This cheat sheet gives you a run down of the common operations first, and the list-specific operations second.

### Common sequence operations
len(sequence) Returns the length of the sequence

for element in sequence Iterates over each element in the sequence

if element in sequence Checks whether the element is part of the sequence

sequence[i] Accesses the element at index i of the sequence, starting at zero

sequence[i:j] Accesses a slice starting at index i, ending at index j-1. If i is omitted, it's 0 by default. If j is omitted, it's len(sequence) by default.

for index, element in enumerate(sequence) Iterates over both the indexes and the elements in the sequence at the same time

 Check out the official documentation for sequence operations.

### List-specific operations and methods
list[i] = x Replaces the element at index i with x

list.append(x) Inserts x at the end of the list

list.insert(i, x) Inserts x at index i

list.pop(i) Returns the element a index i, also removing it from the list. If i is omitted, the last element is returned and removed.

list.remove(x) Removes the first occurrence of x in the list

list.sort() Sorts the items in the list

list.reverse() Reverses the order of items of the list

list.clear() Removes all the items of the list

list.copy() Creates a copy of the list

list.extend(other_list) Appends all the elements of other_list at the end of list

 Most of these methods come from the fact that lists are mutable sequences. For more info, see the official documentation for mutable sequences and the list specific documentation.

### List comprehension
[expression for variable in sequence] Creates a new list based on the given sequence. Each element is the result of the given expression.

[expression for variable in sequence if condition] Creates a new list based on the given sequence. Each element is the result of the given expression; elements only get added if the condition is true.  

## Modifying Lists
While lists and strings are both sequences, a big difference between them is that **lists are mutable**.
This means that the contents of the list can be changed, unlike **strings, which are immutable**.
You can add, remove, or modify elements in a list.

You can add elements to the end of a list using the **append** method.
You call this method on a list using dot notation, and pass in the element to be added as a parameter.
For example, **list.append("New data")** would add the string "New data" to the end of the list called list.

If you want to add an element to a list in a specific position,
you can use the method **insert**. The method takes two parameters:
the first specifies the index in the list, and the second is the element to be added to the list.
So **list.insert(0, "New data")** would add the string "New data" to the front of the list.
This wouldn't overwrite the existing element at the start of the list.
It would just shift all the other elements by one.
If you specify an index that’s larger than the length of the list,
the element will simply be added to the end of the list.

You can remove elements from the list using the **remove** method.
This method takes an element as a parameter, and removes the first occurrence of the element.
If the element isn’t found in the list, you’ll get a **ValueError** error explaining that the element was not found in the list.

You can also remove elements from a list using the **pop** method.
This method differs from the remove method in that it takes an index as a parameter,
and returns the element that was removed.
This can be useful if you don't know what the value is, but you know where it’s located.
This can also be useful when you need to access the data and also want to remove it from the list.

Finally, you can change an element in a list by using indexing to overwrite the value stored at the specified index.
For example, you can enter **list[0] = "Old data"** to overwrite the first element in a list with the new string "Old data".