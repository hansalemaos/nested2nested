# converts a nested list into a nested dictionary with support for multi-level keys and preserving the order

## pip install nested2nested 

#### Tested against Windows 10 / Python 3.10 / Anaconda 


### Conversion of nested lists to nested dictionaries: 

The function provides a convenient way to convert nested lists into nested dictionaries. This can be useful when working with data structures that require a hierarchical representation, such as JSON-like structures or when organizing data in a tree-like format.

### Support for multi-level keys: 

The function utilizes the MultiKeyIterDict class, which allows the use of multi-level keys in the resulting nested dictionary. This means that each level of the nested list can be represented as a key in the corresponding level of the dictionary.

### Preservation of order: 

The MultiKeyIterDict class used in the function preserves the order of elements during conversion. This is important when the order of elements in the nested list needs to be maintained in the resulting dictionary.

### Flexibility and reusability: 

The function is designed to be flexible and can handle nested lists of any depth or structure. It uses a separate module, flatten_any_dict_iterable_or_whatsoever, to flatten the nested list, making it adaptable to various use cases. The MultiKeyIterDict class can also be used independently for other projects involving multi-level dictionaries.

This function can be useful for developers or data analysts working with hierarchical or nested data structures. It simplifies the process of converting nested lists to nested dictionaries and provides flexibility in handling multi-level keys. It can be applied in various domains, including data manipulation, data preprocessing, and working with complex data structures.

```python
from nested2nested import nested_list_to_nested_dict
d = nested_list_to_nested_dict(l=[33, 4, ['baba', 4, ['babx', [[4, 4, 5, 2], 4], 4, 32], 4, 3], 423])
print(d)
{
    0: 33,
    1: 4,
    2: {
        0: 'baba',
        1: 4,
        2: {
            0: 'babx',
            1: {
                0: {
                    0: 4,
                    1: 4,
                    2: 5,
                    3: 2
                },
                1: 4
            },
            2: 4,
            3: 32
        },
        3: 4,
        4: 3
    },
    3: 423
}


```