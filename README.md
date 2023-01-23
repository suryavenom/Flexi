# **DICTIONARIFY**

<!--slockquote-->
### *Installation*
>pip install dictionarify

<!--horizontal rule-->
___

<!--slockquote-->
### *Updation*
run this code in terminal
>pip install dictionarify --upgrade

<!--horizontal rule-->
___
<!--slockquote-->
### *Documentation*
how to get the documentation of the my library and type this in python script

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
print(Flexi.__doc__)
# click the link
```
#or
go to this link https://pypi.org/project/dictionarify/0.0.6/
and click on the link given in project description.

<!--horizontal rule-->
___

## **Introduction**
It is a library which consists of a class called **'Flexi'** which have methods similar to list methods like sort , insert etc for dictionary.

## **METHODS OF dictionarify**
1. **search_all(lists:list,value,index_range:tuple)**:

It returns the index of the first occurrence of the value in the list, or a tuple of all the indices
of the value in the list if the index range is specified
    
* lists: enter the list where you wnat to run this function
* value: the value you want to search for
* index_range: tuple

<!-- Github Markdown -->
<!-- Code Block -->
```python
import dictionarify
'''
in the third argument you have the give the start and stop index in a tuple
'''
'''
when index_range = (0,4) it means it searches from index 0 to index 3.
in second case index_range = (0,2) it means it searches from index0 to index 1
'''
print(dictionarify.search_all([1,2,3,1],1,(0,4)))# (0, 3)

print(dictionarify.search_all([1,2,3,1],1,(0,2)))# (0,)
```

<!--horizontal rule-->
___

## **METHODS OF Flexi**



1.**is_value(self, value):**

It returns True if the value is in the dictionary, and False if it is not.
* value: The value to search for

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2})
print(x.is_value(1)) #True
```

<!--horizontal rule-->
___

2.**is_item(self, key,value):**

The function is_item() takes in a key and a value and returns True if the key and value are in
the dictionary and False if they are not.
* key: The key to search for
* value: The value to be searched for

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2})
print(x.is_item("a",1)) #True
```

<!--horizontal rule-->
___

3. **d_index(self, kev,start_pos:int = None, stop_pos:int = None,condition="key" ):**

It returns the index of the key or value in the dictionary
        
* kev: the key or value you want to search for
* start_pos: The starting index of the search
* stop_pos: The position of the last element to be included in the search
* condition: This is the condition for the search. It can be either "key" or "value", defaults
to key (optional)

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2,"c": 3})
'''
here condition = "key", it means that it will check whether the key exists if it exists then it will return the index of the key between the start_pos and stop_pos else it will show an error
'''
print(x.d_index("c",0,3))#2
'''
here condition = "value", it means that it will check whether the value exists if it exists then it will return the index of the key between the start_pos and stop_pos else it will show an error
'''
print(x.d_index(1,0,3,condition = "value"))#0
```
<!--horizontal rule-->
___

4. **d_get(self,value)**:

If the value is in the dictionary, return the key(s) associated with the value

* value: The value you want to get the key of

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2,"c": 3})
print(x.d_get(1))# a
```
<!--horizontal rule-->
___

5. **d_key(self, index: int)**:

It returns the key of the dictionary at the given index

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2,"c": 3})
print(x.d_key(1))# b
```
<!--horizontal rule-->
___

6. **d_value(self, index: int)**:

It returns the value of the dictionary at the given index

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2,"c": 3})
print(x.d_value(1))# 2
```
<!--horizontal rule-->
___

7. **d_item(self, index: int)**:

It returns the item at the given index in the dictionary

<!-- Github Markdown -->
<!-- Code Block -->
```python
from dictionarify import Flexi
x = Flexi({"a": 1, "b": 2,"c": 3})
print(x.d_item(1))# ('b', 2)
```
<!--horizontal rule-->
___

8. **d_exchange(self, no_of_exchanges=1,entanglement = True, return_type="no_update")**:

It exchanges the keys and values of a dictionary
        
* no_of_exchanges: the number of times the dictionary is exchanged, defaults to 1 (optional),
defaults to 1 (optional)
* entanglement: if True, it will exchange the dictionary even if it has identical values,
defaults to True (optional) else it will show error message.
* return_type: if you want to update the dictionary or not, defaults to no_update (optional),
defaults to no_update (optional)
<!--horizontal rule-->
___

> # *Note*:
>* the argument return_type is in many methods like this however it serves the same function /task i.e to update the dictionary or not update the dictionary/return the dictionary.
>* If you want to update the dictionary just set return_type = "update".
>* It is always defaulted to "no_update".
<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3}
x = Flexi(dictionary)
print(x.d_exchange())# {1: 'a', 2: 'b', 3: 'c'}
print(dictionary)# {'a': 1, 'b': 2, 'c': 3}
print(x.d_exchange(return_type="update"))# None
print(dictionary)# {1: 'a', 2: 'b', 3: 'c'}
'----------------------------------------------'
y = Flexi({"a":1,"b":2,"c":1})
print(y.d_exchange(entanglement=True))# {'b': 2, ('a', 'c'): 1}
print(y.d_exchange(entanglement=False))# Exception: the dictionary has identical values so it cannot be exchanged
```
<!--horizontal rule-->
___

9. **d_reverse(self, no_of_times=1, return_type="no_update")**:

It reverses the dictionary and returns the reversed dictionary. 

* no_of_times: The number of times you want to reverse the dictionary, defaults to 1 (optional)
* return_type: If you want to update the dictionary, then set return_type to "update". If you
want to return a new dictionary, then set return_type to "no_update", defaults to no_update

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3}
x = Flexi(dictionary)
print(x.d_reverse())# {'c': 3, 'b': 2, 'a': 1}

```
<!--horizontal rule-->
___

10. **sort_keys(self, return_type="no_update")**:

It takes a dictionary, sorts it by key

* return_type: This is the type of return value you want. If you want the dictionary to be
updated, then you should pass "update" as the value. If you want a new dictionary to be returned,
then you should pass "no_update" as the value, defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3}
x = Flexi(dictionary)
print(x.sort_keys())# {'a': 2, 'b': 3, 'd': 1}

```
<!--horizontal rule-->
___


11. **sort_values(self, return_type="no_update")**:

It sorts the values of the dictionary.
* return_type: This is the type of return value you want. If you want the dictionary to be
updated, then you should pass "update" as the value. If you want a new dictionary to be returned,
then you should pass "no_update" as the value, defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 3, "b": 2,"c": 1}
x = Flexi(dictionary)
print(x.sort_values())# {'c': 1, 'b': 2, 'a': 3}

```
<!--horizontal rule-->
___

12. **d_insert(self, index: int, key, value, return_type="no_update")**:

it inserts key:value into the dictionary.
* index: the index where you want to insert the key-value pair

* key: The key to be inserted
* value: The value to be inserted
* return_type: if you want to update the dictionary or not, defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "c": 3,"d": 4}
x = Flexi(dictionary)
print(x.d_insert(1,"b",2))# {'a': 1, 'b': 2, 'c': 3, 'd': 4}

```
<!--horizontal rule-->
___

13. **d_remove(self, index_list: int,return_type: str = "no_update")**:

It takes the dictionary, and then removes the key at the index
* index: the index of the item to be removed
* return_type: If it is "update", then the dictionary is updated. If it is "no_update", then a
new dictionary is returned, defaults to no_update

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3}
x = Flexi(dictionary)
print(x.d_remove(1))# {'a': 1, 'c': 3}
```
<!--horizontal rule-->
___

14. **d_replace(self, index: int, key, value, return_type="no_update")**:

It inserts a new key-value pair at the specified index, and then removes the key-value pair that was
previously at that index
        
* index: The index of the key-value pair you want to replace
* key: The key to be replaced
* value: The value to be inserted
* return_type: This is the type of return value you want. If you want the dictionary to be
updated, then you should use "update". If you want a new dictionary to be returned, then you should
use "no_update", defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "d": 4,"c": 3}
x = Flexi(dictionary)
print(x.d_replace(1,"b",2))#{'a': 1, 'b': 2, 'c': 3}
```
<!--horizontal rule-->
___

15. **d_slicing(self, start_index:int=None, stop_index:int=None, step_index:int=None, return_type="no_update")**:

It takes a dictionary, slices it, and returns a new dictionary
        
* start_index: The starting index of the slicing. Default is 0
* stop_index: The index of the last element in the list
* step_index: The step size of the slicing. Default is 1
* return_type: if you want to update the dictionary, then set it to "update", else set it to
"no_update", defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
x = Flexi({"a":1,"b":2,"c":3,"d":4,"e":5})
print(x.d_slicing(0,4))# {'a': 1, 'b': 2, 'c': 3, 'd': 4} 
```
<!--horizontal rule-->
___

16. **swap_keys(self, initial_index: int, final_index: int, return_type="no_update")**:
It swaps the keys of the dictionary at the given indices
        
* initial_index: the index of the key you want to swap
* final_index: the index of the key you want to swap with the initial_index key
* return_type: if you want to update the dictionary, then you should pass "update" as the
return_type, defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.swap_keys(0,4))#{'e': 1, 'b': 2, 'c': 3, 'd': 4, 'a': 5}
```
<!--horizontal rule-->
___

17. **swap_values(self, initial_index: int, final_index: int, return_type="no_update")**:

It swaps the values of two keys in a dictionary
        
* initial_index: the index of the first value to be swapped
* final_index: the index of the value you want to swap with the value at initial_index
* return_type: if you want to update the dictionary, set it to "update", otherwise, set it to
"no_update", defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.swap_values(0,4))# {'a': 5, 'b': 2, 'c': 3, 'd': 4, 'e': 1}
```
<!--horizontal rule-->
___

18. **count_value(self, value)**:

It returns the number of times a value appears in the dictionary
        
* value: The value to be counted

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.count_value(1))# 2 
```
<!--horizontal rule-->
___

19. **has_similar_value(self, value)**:

If the value is present in the dictionary, and the count of the value is greater than 1, then return True, otherwise return False
        
* value: The value to be checked for similarity

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.has_similar_value(1))# True
```
<!--horizontal rule-->
___

20. **similar_values(self, value)**:

It returns a dictionary of all the keys and values that have the same value as the value you pass to
the function
        
* value: The value to be searched for

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.similar_values(1))# {'a': 1, 'd': 1}
```
<!--horizontal rule-->
___

21. d_split(self,stop_index:int):

It takes a dictionary and splits it into two dictionaries, the first one containing the first half
of the original dictionary and the second one containing the second half of the original dictionary
        
* stop_index: The index at which the dictionary is split

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c": 3,"d": 4,"e": 5}
x = Flexi(dictionary)
print(x.d_split(1))# ({'a': 1}, {'b': 2, 'c': 3, 'd': 1})
```
<!--horizontal rule-->
___

22. **auto_arrange(self,index_list:list,return_type = "no_update")**:

It takes a list of indices and returns a dictionary with the keys in the same order as the indices
        
* index_list: list of indices in the order you want to arrange the dictionary
* return_type: If you want to update the dictionary, set this to "update". If you want to
return a new dictionary, set this to "no_update", defaults to no_update (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2,"c":3,"d":1}
x = Flexi(dictionary)
'''
you can either pass the entire index of the elements in the dictionary or you can just give some indexes rest be filled automatically.
'''
print(x.auto_arrange([3,0,1,2]))# {'d': 1, 'a': 1, 'b': 2, 'c': 3}
print(x.auto_arrange([3]))# {'d': 1, 'a': 1, 'b': 2, 'c': 3}
```
<!--horizontal rule-->
___

23. **d_max(self,condition="key")**:

It returns the key-value pair of the maximum value in the dictionary
        
condition: This is the condition for the return type. It can be either key or value, defaults
to key (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3, "d": 1}
x = Flexi(dictionary)
'''
if condition == "key" then it will return item with the maximum key in the dictionary else if the condition=="value" then it will return the item with maximum value
'''

print(x.d_max())# {'d': 1}
print(x.d_max(condition="value"))# {'c': 3}
```
<!--horizontal rule-->
___

24. **d_min(self,condition="key")**:

It returns the minimum value of the dictionary, and if there are multiple minimum values, it returns
all the keys associated with the minimum value
* condition: This is the condition for the return type. It can be either key or value, defaults
to key (optional)

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3, "d": 1}
x = Flexi(dictionary)
'''
if condition == "key" then it will return item with the manimum key in the dictionary else if the condition=="value" then it will return the item with manimum value
'''

print(x.d_min())# {'a': 1}
print(x.d_min(condition="value"))# {'a': 1, 'd': 1}
```
<!--horizontal rule-->
___

25. **d_type(self)**:

It returns a dictionary with the same keys as the original dictionary, but the values are the types
of the original values.

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3, "d": 1}
x = Flexi(dictionary)
print(x.d_type())# {'a': <class 'int'>, 'b': <class 'str'>, 'c': <class 'list'>, 'd': <class 'dict'>}
```
<!--horizontal rule-->
___

26. **d_group(self)**:

It takes a dictionary and returns a tuple of dictionaries, in which the key:value pairs are grouped/segregated based on the value types

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3, "d": 1}
x = Flexi(dictionary)
print(x.d_group())# ({'c': [1, 2, 3]}, {'a': 1}, {'d': {'a': 1}}, {'b': 'hello'})
```
<!--horizontal rule-->
___

27. **is_common_key(self,other_dictionary:dict,key)**:

If the key is in both dictionaries, return True. Otherwise, return False
        
* other_dictionary: The dictionary to compare to
* key: the key to check

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"a":1}
print(x.is_common_key(y,"a"))#True
```
<!--horizontal rule-->
___

28. **is_common_value(self,other_dictionary:dict,value)**:
It checks if the value is present in both the dictionaries.
        
* other_dictionary: The dictionary to compare with
* value: The value to check for

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"a":1}
print(x.is_common_value(y,1))#True
```
<!--horizontal rule-->
___

29. **is_common_item(self,other_dictionary:dict,key,value)**:

If the key and value are in both dictionaries, return True
        
* other_dictionary: The dictionary to compare with
* key: the key to check
* value: The value of the key

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"a":1}
print(x.is_common_item(y,"a",1))#True
```
<!--horizontal rule-->
___

30. **item_with_common_key(self,other_dictionary:dict)**:

It takes a dictionary as an argument and returns a tuple of dictionaries containing the common keys
        and their values
        
* other_dictionary: The dictionary that you want to compare with

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"a":100}
print(x.item_with_common_key(y))# ({'a': 1}, {'a': 100})
```
<!--horizontal rule-->
___

31. **item_with_common_value(self,other_dictionary:dict)**:

It returns a tuple of dictionaries of the keys that have the same value in both dictionaries.
        
* other_dictionary: The dictionary that you want to compare with the dictionary that you have
created the object with

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"apple":1}
print(x.item_with_common_value(y))# ({'a': 1}, {'apple': 1})
```
<!--horizontal rule-->
___

32. **common_item(self,other_dictionary:dict)**:

It takes two dictionaries as input and returns a tuple of dictionaries that have the same key and
value
        
*  other_dictionary: The dictionary to be compared with the current dictionary

<!-- Github Markdown -->
<!-- Code Block -->
<!--horizontal rule-->
___

```python
from dictionarify import Flexi
dictionary = {"a": 1, "b": 2, "c": 3}
x = Flexi(dictionary)
y = {"a":1}
print(x.common_item(y))# ({'a': 1}, {'a': 1})
```
<!--horizontal rule-->
___

## **Author:-** *Surya Narayanan K V*
## **Credits:-** *Riswan*,*Kannan*,*Sreeja mam*
