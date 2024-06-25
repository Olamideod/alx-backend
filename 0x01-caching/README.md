# Caching Project

## Overview

This project focuses on implementing various caching algorithms in Python. Caching is a critical optimization technique used to speed up data retrieval processes by storing copies of frequently accessed data in faster storage.

## Learning Objectives

By the end of this project, you should be able to:

- Understand what a caching system is.
- Explain the following caching algorithms:
  - FIFO (First In, First Out)
  - LIFO (Last In, First Out)
  - LRU (Least Recently Used)
  - MRU (Most Recently Used)
  - LFU (Least Frequently Used)
- Describe the purpose and limitations of a caching system.

## Resources

To complete this project, you should read or watch the following resources:

- Cache replacement policies - FIFO
- Cache replacement policies - LIFO
- Cache replacement policies - LRU
- Cache replacement policies - MRU
- Cache replacement policies - LFU

## Requirements

### Python Scripts

- All files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7.
- All files should end with a new line.
- The first line of all files should be exactly `#!/usr/bin/env python3`.
- A `README.md` file, at the root of the project folder, is mandatory.
- Code must follow the `pycodestyle` style guide (version 2.5).
- All files must be executable.
- The length of files will be tested using `wc`.
- All modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`).
- All classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`).
- All functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'` and `python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`).

## Project Structure

### BaseCaching Class

All caching classes will inherit from the `BaseCaching` class defined below:

```python
#!/usr/bin/python3
""" BaseCaching module """

class BaseCaching():
    """ BaseCaching defines:
      - constants of your caching system
      - where your data are stored (in a dictionary)
    """
    MAX_ITEMS = 4

    def __init__(self):
        """ Initialize """
        self.cache_data = {}

    def print_cache(self):
        """ Print the cache """
        print("Current cache:")
        for key in sorted(self.cache_data.keys()):
            print("{}: {}".format(key, self.cache_data.get(key)))

    def put(self, key, item):
        """ Add an item in the cache """
        raise NotImplementedError("put must be implemented in your cache class")

    def get(self, key):
        """ Get an item by key """
        raise NotImplementedError("get must be implemented in your cache class")

