Class Flexi is a python class that provides various functionalities to work with dictionaries in an easy and efficient way. The class takes a dictionary as an input and performs various operations on it. Some of the operations provided by the class are as follows:

d_slicing: This method returns a subset of the dictionary based on the start index, stop index and step size provided.
d_get: This method returns the value of a specific key in the dictionary.
d_index: This method returns the index of a specific key or value in the dictionary.
d_key: This method returns the key of a specific index in the dictionary.
d_value: This method returns the value of a specific index in the dictionary.
is_key: This method checks if a specific key is present in the dictionary.
is_value: This method checks if a specific value is present in the dictionary.
is_item: This method checks if a specific key-value pair is present in the dictionary.
d_remove: This method removes a specific key-value pair from the dictionary.
swap_keys: This method swaps the keys of two specific indices in the dictionary.
swap_values: This method swaps the values of two specific indices in the dictionary.
count_value: This method counts the number of occurrences of a specific value in the dictionary.
has_similar_value: This method checks if there are multiple occurrences of a specific value in the dictionary.
similar_values: This method returns a dictionary containing all key-value pairs with a specific value.
d_split: This method splits the dictionary into two parts based on the stop index provided.
auto_arrange: This method rearranges the dictionary based on the indices provided in the index_list.
d_max: This method returns the maximum key-value pair or maximum value in the dictionary based on the condition provided.
d_min: This method returns the minimum key-value pair or minimum value in the dictionary based on the condition provided.
d_type: This method returns a new dictionary where the values are replaced with their data types.
d_group: This method groups the elements of the dictionary based on their data types.
is_common_key: This method checks if a specific key is present in both the current dictionary and another dictionary provided.
is_common_value: This method checks if a specific value is present in both the current dictionary and another dictionary provided.
is_common_item: This method checks if a specific key-value pair is present in both the current dictionary and another dictionary provided.
item_with_common_key: This method returns a tuple of dictionaries containing key-value pairs with common keys in both the current dictionary and another dictionary provided.
item_with_common_value: This method returns a tuple of dictionaries containing key-value pairs with common values in both the current dictionary and another dictionary provided.
common_item: This method returns a tuple of key-value pairs common in both the current dictionary and another dictionary provided.
All the above methods have an optional parameter 'return_type' which can take two values 'update' or 'no_update'. 'update' updates the current dictionary with the result of the operation and 'no_update' returns the result of the operation without updating the current dictionary. By default, the return_type is 'no_update'.
