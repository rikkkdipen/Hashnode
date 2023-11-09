---
title: "Day 15: Mastering Data Formats: JSON and YAML Explained in Python"
seoTitle: "Day 15: Mastering Data Formats: JSON and YAML Explained in Python"
seoDescription: "JSON is a format for representing data as text. It looks like a collection of key-value pairs, similar to Python dictionaries..."
datePublished: Thu Nov 09 2023 06:30:09 GMT+0000 (Coordinated Universal Time)
cuid: cloqt7ohd000i09jscfem01m7
slug: day-15-mastering-data-formats-json-and-yaml-explained-in-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699424787775/c5759eac-5c8b-4a37-98b7-8fb590e82c51.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699424832399/64b96f21-de3a-4864-9171-1d9e01f1e3ff.png
tags: python, python3, coding, devops, trainwithshubham

---

### JSON in Python

### **What is JSON?**

JSON is a format for representing data as text. It looks like a collection of key-value pairs, similar to Python dictionaries. It's used for structuring data in a way that both humans and computers can easily understand.

### **Basic Structure of JSON**

In JSON, data is organized into objects (similar to Python dictionaries) and arrays (similar to Python lists). An object consists of key-value pairs enclosed in curly braces `{}`, and an array is a list of values enclosed in square brackets `[]`.

### **Data Types in JSON**

JSON supports common data types like strings, numbers, boolean values, null, objects, and arrays.

1. **Example**: Here's a simple JSON object representing information about a person:
    
    ```json
    {
        "name": "Alice",
        "age": 30,
        "isStudent": false,
        "hobbies": ["reading", "swimming"],
        "address": {
            "city": "New York",
            "zipCode": "10001"
        }
    }
    ```
    
    In this JSON object, "name," "age," "isStudent" are key-value pairs, "hobbies" is an array, and "address" is an object.
    
2. **Using JSON in Python**: You can work with JSON data in Python using the built-in `json` module. You can read JSON from a file, convert JSON to Python objects (like dictionaries), and vice versa.
    

### YAML in Python

### What is YAML?

YAML (YAML Ain't Markup Language) is a human-readable data format that is often used for configuration files in Python and other programming languages. It's designed to be easy for both humans and machines to read and write. Here's a simple explanation of YAML in Python:

**1\. Human-Readable:** YAML files are easy for people to read and write. It uses indentation and simple punctuation marks like colons and dashes to structure data.

**2\. Key-Value Pairs:** YAML represents data as key-value pairs, where keys are on the left side of a colon, and values are on the right. For example:

```yaml
name: John
age: 30
city: New York
```

**3\. Hierarchical Structure:** YAML allows you to represent hierarchical or nested data. You can use indentation to indicate the level of nesting. For example:

```yaml
person:
  name: John
  age: 30
  address:
    city: New York
    street: 123 Main St
```

**4\. Lists:** YAML can represent lists of items using a dash `-`. For example:

```yaml
codefruits:
  - apple
  - banana
  - orange
```

**5\. Comments:** You can add comments in YAML files using the `#` symbol. Comments are ignored by parsers and are just for human reference.

```yaml
# This is a comment
name: John
```

### Reading JSON and YAML in Python

JSON (JavaScript Object Notation) is a common data format that Python can easily work with. You can read JSON files using the built-in `json` module. Here's how it works:

1. **Import the** `json` **module:** You need to import the `json` module at the beginning of your Python script.
    
    ```python
    import json
    ```
    
2. **Open and Read the JSON File:** Use the `open()` function to open a JSON file and then use the `json.load()` method to read its contents.
    
    ```python
    open('your_file.json', 'r') as file:
        data = json.load(file)
    ```
    
3. **Use the Data:** Once you've loaded the JSON data, you can use it as a Python dictionary.
    
    For example, if your JSON file contains data like this:
    
    ```bash
    {
        "name": "John",
        "age": 30,
        "city": "New York"
    }
    ```
    
    You can access the values in Python like this:
    
    ```bash
    print(data["name"])  # Output: John
    print(data["age"])   # Output: 30
    print(data["city"])  # Output: New York
    ```
    

**Reading YAML Files in Python:**

YAML (YAML Ain't Markup Language) is another format to represent data, often used in configuration files. You can read YAML files in Python using the `PyYAML` library.

Here's how you can do it:

1. **Install PyYAML:** First, you need to install the `PyYAML` library if you haven't already. You can do this using pip:
    
    ```bash
    pip install pyyaml
    ```
    
2. **Import the PyYAML module:** Import the `yaml` module to work with YAML files.
    
    ```python
    import yaml
    ```
    
3. **Open and Read the YAML File:** Use the `open()` function to open a YAML file and the `yaml.load()` method to read its contents.
    
    ```python
    open('your_file.yaml', 'r') as file:
        data = yaml.load(file, Loader=yaml.FullLoader)
    ```
    
4. **Use the Data:** Once you've loaded the YAML data, you can use it like a regular Python dictionary or list, depending on the structure of the YAML file.
    
    If your YAML file looks like this:
    
    ```yaml
    codename: John
    age: 30
    city: New York
    ```
    
    You can access the values in Python similarly to how you did with JSON:
    
    ```python
    print(data["name"])  # Output: John
    print(data["age"])   # Output: 30
    print(data["city"])  # Output: New York
    ```
    

That's it! You can now read both JSON and YAML files in Python and work with the data as needed in your programs.

### Tasks:

1. Create a Dictionary in Python and write it to a json File.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699423860060/e3dadb50-59a3-4a7f-89ca-8b68abf52f9a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699424076760/e2205c65-8c96-4a1c-983b-8a48d58b32e1.png align="center")

1. Read a json file `services.json` kept in this folder and print the service names of every cloud service provider.
    

```json
{
  "aws": "ec2",
  "azure": "VM",
  "gcp": "compute engine"
}
```

You can use the following Python code:

```python
import json

# Read the JSON file
with open('services.json', 'r') as json_file:
    data = json.load(json_file)

# Iterate through the cloud service providers and their services
for provider, service in data.items():
    print(f"{provider} : {service}")
```

When you run this code, it will read the "services.json" file, load its content, and then iterate through the dictionary, printing the cloud service provider and its associated service. The output will be as you described:

```yaml
codeaws : ec2
azure : VM
gcp : compute engine
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699424359820/16c50b3b-3081-4fba-b3b9-01d3ecacb98c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699424370511/124f54e8-0ee7-4cff-acd4-dd310af3c4f1.png align="center")

Make sure the "services.json" file is located in the same directory where your Python script is running. You can adjust the file path if it's located in a different directory.

1. Read YAML file using python, file `services.yaml` and read the contents to convert yaml to json
    

To read a YAML file in Python and convert its contents to JSON, you can use the `PyYAML` library to read the YAML data and then use the `json` module to convert it to JSON. Here's how you can do it:

1. First, install the `PyYAML` library if you haven't already. You can do this using pip:
    
    ```python
    pip install pyyaml
    ```
    
2. Next, create a Python script to read the YAML file and convert its contents to JSON.
    

Assuming your "services.yaml" file contains data like this:

```yaml
codeaws: ec2
azure: VM
gcp: compute engine
```

You can use the following Python code:

```python
import yaml
import json

# Read the YAML file
with open('services.yaml', 'r') as yaml_file:
    data = yaml.load(yaml_file, Loader=yaml.FullLoader)

# Convert YAML to JSON
json_data = json.dumps(data)

# Print the JSON data
print(json_data)
```

This code will read the "services.yaml" file, load its content using `PyYAML`, and then convert it to JSON using the `json` module. The JSON representation of the YAML data will be printed to the console.

Make sure the "services.yaml" file is located in the same directory where your Python script is running, or provide the correct file path if it's located in a different directory.

Hope this will help you in your better understanding about JSON and YAML in python If you like my work do follow, like and share.

You can also connect with me:

Github: [**https://github.com/dipen006**  
Twitter](https://github.com/dipen006￼Twitter): [**https://twitter.com/dipenr06**  
Linkedin](https://twitter.com/dipenr06￼Linkedin): [**https://www.linkedin.com/in/dipenr06/**](https://www.linkedin.com/in/dipenr06/)