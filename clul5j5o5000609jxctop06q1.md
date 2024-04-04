---
title: "Day 13: What is Python and different data types in python?"
seoTitle: "What is Python and different data types in python?"
seoDescription: "What is Python and different data types in python?"
datePublished: Thu Apr 04 2024 11:26:37 GMT+0000 (Coordinated Universal Time)
cuid: clul5j5o5000609jxctop06q1
slug: day-13-what-is-python-and-different-data-types-in-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1712229889446/f5b8056b-75bf-4835-8f6c-e2e41be8aae0.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1712229957174/03e711c8-cb6c-4d87-ba0e-73d383a0a00d.png
tags: ubuntu, linux, python, development, developer, python3, devops, hashnode, pip, devops-articles, 90daysofdevops, wemakedevs, trainwithshubham

---

Python is a type of computer language that people use to tell computers what to do. It's like giving instructions to your computer so it can perform tasks. Python is known for being easy to understand and write, making it popular for beginners and professionals alike.

Guido van Rossum, a Dutch programmer, created Python. He started working on Python in the late 1980s and officially released it in 1991. Guido van Rossum aimed to make a programming language that was easy to read and write, like plain English.

Python consists of different elements that help in writing instructions for computers. These include:

1. **Syntax:** Rules and structure for writing Python code.
    
2. **Functions:** Pre-written pieces of code that perform specific tasks.
    
3. **Libraries:** Collections of functions and tools for specific purposes, like web development, data analysis, or artificial intelligence.
    
4. **Variables:** Names used to store data that can be used and changed in the code.
    
5. **Loops and Conditions:** Control structures that let you repeat tasks or make decisions in your code.
    

Overall, Python is like a toolbox full of easy-to-use tools that help you build all kinds of things with your computer, whether it's websites, games, analyzing data, or automating tasks.

## How to install Python?

### How to install Python in Windows?

1. **Go to the Python website:** Open your web browser and go to [www.python.org](http://www.python.org).
    
2. **Download** **Python:** On the Python website, click on the "Downloads" tab. You'll see a button that says "Download Python." Click on it.
    
3. **Choose the installer:** You'll be directed to a page with different versions of Python. The latest version is usually displayed at the top. Click on the "Download" button next to the version you want. For most users, the recommended version is fine.
    
4. **Run the installer:** Once the download is complete, find the downloaded file (it's usually in your Downloads folder) and double-click on it to run the installer.
    
5. **Start the installation:** A window will pop up with options for installing Python. Make sure to check the box that says "Add Python to PATH." This option makes it easier to run Python commands from the Command Prompt. Then, click "Install Now" to start the installation process.
    
6. **Wait for installation:** The installer will then install Python on your computer. This may take a few minutes, so be patient.
    
7. **Finish installation:** Once the installation is complete, you'll see a message saying "Setup was successful." Click on the "Close" button to exit the installer.
    
8. **Verify installation:** To make sure Python installed correctly, open the Command Prompt by typing "cmd" in the Windows search bar and pressing Enter. Then, type "python" and press Enter. You should see a message with the Python version number, and the Python interactive shell should open.
    

That's it! Python is now installed on your Windows computer, and you're ready to start coding. You can close the Command Prompt for now, and whenever you want to write and run Python code, just open the Command Prompt again and start typing your commands.

### How to install python in Linux?

1. **Open Terminal:** Launch the Terminal on your Linux system. You can usually find it by searching for "Terminal" in the applications menu.
    
2. **Update package list:** It's a good practice to update your package list before installing new software. Type the following command in the Terminal and press Enter:
    
    ```plaintext
    sudo apt update
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1712229618506/a20c9d52-d786-4f4d-b8ba-c3be887194d3.png align="center")
    
3. **Install Python:** Most Linux distributions come with Python pre-installed, but if it's not, you can install it easily using the package manager. In the Terminal, type the following command and press Enter:
    
    ```plaintext
    sudo apt install python3
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1712229644209/7fd82c12-8430-456b-b76d-df4b93be8120.png align="center")
    
    This command will install Python 3, which is the latest version. If you specifically need Python 2, you can replace "python3" with "python" in the command.
    
4. **Verify installation:** Once the installation is complete, you can verify that Python is installed correctly by typing the following command in the Terminal and pressing Enter:
    
    ```plaintext
    python3 --version
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1712229661987/bb791679-416e-46f6-beac-2f6d8bc7e808.png align="center")
    
    This command will display the version number of Python installed on your system.
    
5. **Optional: Install pip:** Pip is a package manager for Python that allows you to easily install and manage Python libraries and dependencies. To install pip, type the following command in the Terminal and press Enter:
    
    ```plaintext
    sudo apt install python3-pip
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1712229686231/26be962f-5de1-446c-9c11-60fba10e7e8f.png align="center")
    
6. **Verify pip installation (optional):** You can verify that pip is installed correctly by typing the following command in the Terminal and pressing Enter:
    
    ```plaintext
    pip3 --version
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1712229703698/b9bf461a-829c-4308-ae8c-8e84f4e5bd69.png align="center")
    
    This command will display the version number of pip installed on your system.
    

That's it! Python is now installed on your Linux system, and you're ready to start coding. You can close the Terminal, and whenever you want to write and run Python code, just open the Terminal again and start typing your commands.

### Data Types in Python

1. **Integer (int):** Integers are whole numbers without any decimal point. For example, 5, -10, and 1000 are integers.
    
2. **Float (float):** Floats are numbers with decimal points. For example, 3.14, -0.5, and 2.71828 are floats.
    
3. **String (str):** Strings are sequences of characters, enclosed within single (' ') or double (" ") quotes. For example, "Hello, world!", 'Python', and "123" are strings.
    
4. **Boolean (bool):** Booleans represent truth values, either True or False. Booleans are often used for conditions and comparisons in programming.
    
5. **List:** Lists are ordered collections of items, separated by commas and enclosed within square brackets (\[\]). Lists can contain elements of different data types. For example, \[1, 2, 3\], \['apple', 'banana', 'orange'\], and \[1, 'hello', True\] are lists.
    
6. **Tuple:** Tuples are similar to lists but are immutable, meaning they cannot be changed after creation. Tuples are enclosed within parentheses (()). Example: (1, 2, 3), ('a', 'b', 'c'), and (True, False, True) are tuples.
    
7. **Dictionary (dict):** Dictionaries are collections of key-value pairs, enclosed within curly braces ({}). Each key is associated with a value. Keys are unique within a dictionary, but values can be duplicated. Example: {'name': 'John', 'age': 30, 'city': 'New York'} is a dictionary.
    
8. **Set:** Sets are unordered collections of unique elements, enclosed within curly braces ({}). Sets do not allow duplicate values. Example: {1, 2, 3}, {'apple', 'banana', 'orange'}, and {True, False} are sets.
    

These are some of the basic data types in Python. Understanding them is essential for working with data and writing effective Python code

~Dipen : )