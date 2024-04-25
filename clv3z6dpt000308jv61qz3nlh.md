---
title: "Day 15: Python Power-Ups: Must-Have Libraries for DevOps Mastery!"
seoTitle: "Python Power-Ups: Must-Have Libraries for DevOps Mastery!"
seoDescription: "Maximize DevOps efficiency with Python's essential libraries! Streamline automation, manage infrastructure effortlessly, and deploy with ease."
datePublished: Wed Apr 17 2024 15:36:21 GMT+0000 (Coordinated Universal Time)
cuid: clv3z6dpt000308jv61qz3nlh
slug: day-15-python-power-ups-must-have-libraries-for-devops-mastery
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1713366358739/3a582076-9572-4478-a215-84c0acadde55.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1713366611829/a5813904-a850-4095-936e-ebc02a716916.png
tags: linux, programming, python, kubernetes, developer, python3, devops, hashnode, python-beginner, linux-for-beginners, devops-articles, 90daysofdevops, trainwithshubham

---

### JSON in Python

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. In Python, the `json` library allows you to work with JSON data seamlessly.

Now, how does this relate to DevOps? Well, in DevOps, you often deal with automating processes, managing configurations, and exchanging data between different systems. JSON is commonly used in DevOps for configuration files, API requests and responses, and exchanging data between different tools and services.

With the `json` library in Python, you can easily read JSON data from files or network requests, manipulate it, and then convert it back to JSON format when needed. This makes it very handy for tasks like configuring servers, managing infrastructure, or integrating different services together in a DevOps pipeline.

### YAML in Python

YAML is a format for writing data in a way that's easy for humans to read and write. In Python, the YAML library allows you to work with YAML files, which are commonly used in DevOps for configuration files, data serialization, and communication between different systems.

Imagine you have a bunch of settings for your software stored in a file. Instead of using something like JSON, which can get a bit messy with all those curly braces and quotes, YAML lets you write it in a more organized and human-readable way.

Here's a simple example of YAML:

```yaml
database:
  host: localhost
  port: 3306
  username: admin
  password: admin@123
```

In Python, you can use the YAML library to read this file and convert it into a Python dictionary, which you can then use in your code. Similarly, you can take a Python dictionary and convert it into a YAML file.

So, in DevOps, you might use the YAML library to read configuration files for your infrastructure, like defining server settings, network configurations, or deployment pipelines. It helps keep things organized, readable, and easy to work with across different tools and systems.

### List of few libraries which are used in Devops

here are some commonly used Python libraries in DevOps along with simple explanations:

1. **Paramiko**: Used for SSH connections and executing commands on remote machines.
    
2. **Fabric**: Simplifies remote execution of shell commands and deployment tasks over SSH.
    
3. **Ansible (via Ansible Python API)**: Automation tool for configuration management, deployment, and orchestration of infrastructure.
    
4. **Jinja2**: Templating engine often used with configuration management tools like Ansible.
    
5. **PyYAML**: Allows reading and writing YAML files, commonly used for configuration.
    
6. **Docker SDK for Python (docker)**: Interact with Docker containers and services through Python.
    
7. **boto3**: AWS SDK for Python. Allows interacting with various AWS services programmatically.
    
8. **Terraform SDK for Python (hcl2)**: Interact with Terraform configurations and manage infrastructure as code.
    
9. **Kubernetes SDK for Python (client-python)**: Interact with Kubernetes clusters programmatically.
    
10. **Prometheus Client for Python**: Instrument applications for monitoring with Prometheus.
    
11. **Flask/Django**: Web frameworks for building internal tools, dashboards, or APIs for DevOps tasks.
    
12. **psutil**: Provides utilities for querying system utilization (CPU, memory, disk, network).
    
13. **Pytest**: Framework for writing and running tests. Useful for testing infrastructure code.
    
14. **GitPython**: Interact with Git repositories programmatically for tasks like cloning, pulling, or committing changes.
    
15. **Click**: Framework for creating command-line interfaces (CLIs) for DevOps scripts and tools.
    

### Tasks:

### Create a Dictionary in Python and write it to a JSON file

```python
import json

# Create a dictionary
data = {
    "name": "Dipen",
    "age": 24,
    "city": "Mumbai"
}

# Specify the file name
file_name = "data.json"

# Write dictionary to JSON file
with open(file_name, "w") as json_file:
    json.dump(data, json_file, indent=4)

print("Data has been written to", file_name)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713364145389/33ca00e1-9fa1-4e01-9fb9-33aaa299ad10.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713364192904/cc997152-4057-4579-b625-9789db9263c6.png align="center")

In this code:

* We import the `json` module which provides functions for working with JSON data.
    
* We create a dictionary named `data` with some key-value pairs.
    
* We specify the file name as "data.json".
    
* We open the file in write mode (`"w"`) using `open()` function along with a `with` statement, ensuring the file is properly closed after writing.
    
* We used `json.dump()` to write the dictionary `data` into the file `json_file`, with an indentation of 4 spaces for better readability.
    
* Finally, we print a message confirming that the data has been written to the file.
    

### Read a JSON file services.json kept in the folder and print the name of every cloud service provider

services.json

```json
{
    "services":{
        "debug" : "on",
        "aws":{
            "name": "EC2",
            "type": "Pay per hour",
            "instance":500,
            "count":500
        },
        "azure":{
            "name": "VM",
            "type": "pay per hour",
            "instance":500,
            "count":500
        },
        "gcp":{
            "name": "Compute Engine",
            "type": "pay per hour",
            "instance":500,
            "count":500
        }
    }
}
```

printcloudproviders.py

```python
import json

with open("services.json", "r") as file:
    data = json.loads(file.read())
    data['services'].pop('debug')

for a, b in data['services'].items():
    print(a+" : "+ b['name'])
```

Output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713365729159/87cd6754-12c5-4576-9c52-cd7152eb8668.png align="center")

### Read the YAML file name as "Services.yaml" using Python, read the content, and convert yaml to JSON

services.yaml

```yaml
services:
  debug: 'on'
  aws:
    name: EC2
    type: pay per hour
    instance: 500
    count: 500
  azure:
    name: VM
    type: pay per hour
    instance: 500
    count: 500
  gcp:
  name: Compute Engine
  type: pay per hour
  instance: 500
  count: 500
```

task3.py

```python
import yaml
from yaml.loader import SafeLoader

with open('services.yaml') as s:
    data = yaml.load(s, Loader=SafeLoader)
    print(data)
```

output

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713366280475/bb5258ad-a85b-4cf6-80ee-df13dc484cc2.png align="center")

> "Fuel my passion and support my journey by clicking '**Buy me a coffee**' today!"

~Dipen : )