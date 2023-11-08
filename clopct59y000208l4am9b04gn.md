---
title: "Day 14: Unlocking the Power of Python Data Types and Data Structures"
seoTitle: "Day 14: Unlocking the Power of Python Data Types and Data Structures"
seoDescription: "Data types in Python represent the different kinds of values that your program can work with....."
datePublished: Wed Nov 08 2023 06:03:11 GMT+0000 (Coordinated Universal Time)
cuid: clopct59y000208l4am9b04gn
slug: day-14-unlocking-the-power-of-python-data-types-and-data-structures
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699423181895/492b2aa7-b27a-44e7-91fd-b860534e6f7b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699423374562/f7671d1c-f3c4-41c7-888f-3146dcf269a9.png
tags: python, data-structures, python3, devops, trainwithshubham

---

### Data Types in Python

Data types in Python represent the different kinds of values that your program can work with. They help Python understand and manage the data you use in your code. Here's a simple explanation of some common data types in Python:

1. **Integer (int)**: Integers are whole numbers without any decimal points. For example, 5, -10, and 0 are integers. You can use them for counting or simple arithmetic.
    
2. **Float (float)**: Floats are numbers with decimal points. For example, 3.14 or -0.5. They are used when you need more precision in your calculations.
    
3. **String (str)**: Strings are sequences of characters, like words or sentences. You can use single (' ') or double (" ") quotes to create strings. For example, "Hello, Python!" is a string.
    
4. **Boolean (bool)**: Booleans represent truth values, and there are only two possible values: True and False. They are often used for making decisions in your code, like in conditional statements (if, else).
    
5. **List**: A list is an ordered collection of items that can be of any data type. You can put multiple values in a list, and they can be changed (mutable). For example, `my_list = [1, 'apple', 3.14, True]`.
    
6. **Tuple**: Tuples are similar to lists but are immutable, which means you can't change their contents once you create them. They are defined using parentheses. For example, `my_tuple = (1, 'apple', 3.14, True)`.
    
7. **Dictionary (dict)**: A dictionary is a collection of key-value pairs. It's like a real-world dictionary, where words (keys) have definitions (values). For example, `my_dict = {'name': 'Alice', 'age': 30}`.
    
8. **Set**: Sets are collections of unique, unordered elements. They are useful for tasks like removing duplicates from a list. For example, `my_set = {1, 2, 3, 4, 2, 3}` would be treated as `{1, 2, 3, 4}`.
    

These data types help Python understand and work with different types of information in your programs. Depending on what you want to do, you can choose the appropriate data type to store and manipulate your data.

To check what is the data type of the variable used, we can simply write:

```bash
variable_n = 100
print(type(variable_n))
```

### Data Structures in Python

Data structures in Python are like containers that allow you to organize and store your data in different ways. They help you manage and manipulate data efficiently. Here's a simple explanation of some common data structures in Python:

1. **List**: A list is an ordered collection of items. Think of it as a sequence of values like numbers, words, or other data. Lists can hold elements of different data types, and you can change their contents (mutable). For example, you can create a list of numbers: `[1, 2, 3]`.
    
2. **Tuple**: A tuple is similar to a list, but it's immutable, which means you can't change its contents after creating it. Tuples are defined using parentheses. For example, you can create a tuple like this: `(1, 2, 3)`.
    
3. **Dictionary (dict)**: A dictionary is like a real-world dictionary, where you have words (keys) and their definitions (values). Dictionaries store key-value pairs and allow you to quickly look up values by their associated keys. For example, you can create a dictionary with names and ages: `{'Alice': 30, 'Bob': 25}`.
    
4. **Set**: A set is an unordered collection of unique elements. It's useful when you want to store a bunch of values but only keep unique ones. For example, you can create a set with unique numbers: `{1, 2, 3}`.
    
5. **Array**: An array is a data structure that holds a fixed number of elements of the same data type. In Python, you can use arrays from the `array` module. They are often used for mathematical operations and can be more memory-efficient than lists for large datasets.
    
6. **Stack**: A stack is a data structure that follows the Last-In-First-Out (LIFO) principle. It's like a stack of plates where you can only take the top plate off. You can push (add) and pop (remove) elements from the top of the stack.
    
7. **Queue**: A queue is a data structure that follows the First-In-First-Out (FIFO) principle. It's like a line of people waiting for something. You can enqueue (add) elements at the back and dequeue (remove) elements from the front.
    

These data structures help you store and organize your data in different ways, depending on your specific needs. They make it easier to perform various operations, search for data, and manage your information effectively in your Python programs.

### Tasks:

1. Give the Difference between List, Tuple and set. Do Handson and put screenshots as per your understanding.
    

1. **List**:
    
    * **Mutability**: Lists are mutable, which means you can change their contents (add, remove, or modify elements) after creating them.
        
    * **Syntax**: Lists are defined using square brackets, like `[1, 2, 3]`.
        
    * **Ordered**: Lists are ordered, meaning the elements have a specific order, and you can access them by their position (index).
        
    * **Duplicates**: Lists can contain duplicate elements.
        
2. **Tuple**:
    
    * **Immutability**: Tuples are immutable, meaning you can't change their contents after creating them. Once you set the elements, they remain fixed.
        
    * **Syntax**: Tuples are defined using parentheses, like `(1, 2, 3)`.
        
    * **Ordered**: Tuples are ordered, just like lists, so elements have a specific order and can be accessed by their index.
        
    * **Duplicates**: Tuples can contain duplicate elements.
        
3. **Set**:
    
    * **Mutability**: Sets are mutable, but their primary feature is that they are designed to store unique elements. You can add and remove elements, but each element can appear only once in a set.
        
    * **Syntax**: Sets are defined using curly braces or the `set()` function, like `{1, 2, 3}` or `set([1, 2, 3])`.
        
    * **Unordered**: Sets are unordered, meaning elements don't have a specific order, and you can't access them by index.
        
    * **Uniqueness**: Sets automatically remove duplicate values, so you can't have duplicates in a set.
        

In simple terms:

* Use a **list** when you need an ordered collection of items that may change.
    
* Use a **tuple** when you want an ordered collection of items that should not change.
    
* Use a **set** when you need to store a unique collection of items, and the order doesn't matter.
    

1. Create the below Dictionary and use Dictionary methods to print your favorite tool just by using the keys of the Dictionary.
    

```bash
fav_tools ={
  1:"Linux",
  2:"Git",
  3:"Docker",
  4:"Kubernetes",
  5:"Terraform",
  6:"Ansible",
  7:"Chef"
}
```

```bash
#answer

fav_tools = {
  1:"Linux",
  2:"Git",
  3:"Docker",
  4:"Kubernetes",
  5:"Terraform",
  6:"Ansible",
  7:"Chef"
}

print(fav_tools[2])

# This will print "Git"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699422739293/feaad82f-386a-4d02-9bf9-1b6baf597c5b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699422756558/8e0307bb-2d2e-4bdf-92d6-8029a4c6aadd.png align="center")

1. Create a List of cloud service providers eg
    

```bash
cloud_providers = ["AWS","GCP","Azure"]
```

Write a program to add `Digital Ocean` to the list of cloud\_providers and sort the list in alphabetical order.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699423035761/1f12003a-0864-4dc0-a656-d774685d97e3.png align="center")

```bash
#Answer

cloud_providers = ["AWS", "GCP", "Azure"]

# Add "Digital Ocean" to the list
cloud_providers.append("Digital Ocean")

# Sort the list alphabetically
cloud_providers.sort()

# Print the updated list
print(cloud_providers)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699423091422/78ba426e-22a9-4382-b9be-010742b7f6b8.png align="center")

Hope this will help you in your better understanding about python data types and data structures. If you like my work do follow, like and share.

You can also connect with me:

Github: [https://github.com/dipen006](https://github.com/dipen006)  
Twitter: [https://twitter.com/dipenr06](https://twitter.com/dipenr06)  
Linkedin: [https://www.linkedin.com/in/dipenr06/](https://www.linkedin.com/in/dipenr06/)