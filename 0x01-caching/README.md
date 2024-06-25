# Caching Project

## Project Overview
This project focuses on implementing different caching algorithms. You will learn how to implement and understand various cache replacement policies including FIFO, LIFO, LRU, MRU, and LFU.

## Learning Objectives
By the end of this project, you should be able to:
- Explain what a caching system is.
- Define and understand the FIFO (First In, First Out) policy.
- Define and understand the LIFO (Last In, First Out) policy.
- Define and understand the LRU (Least Recently Used) policy.
- Define and understand the MRU (Most Recently Used) policy.
- Define and understand the LFU (Least Frequently Used) policy.
- Understand the purpose of a caching system.
- Recognize the limitations of a caching system.

## Resources
- [Cache replacement policies - FIFO](https://en.wikipedia.org/wiki/Cache_replacement_policies#First_In_First_Out_(FIFO))
- [Cache replacement policies - LIFO](https://en.wikipedia.org/wiki/Cache_replacement_policies#Last_In_First_Out_(LIFO))
- [Cache replacement policies - LRU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Least_Recently_Used_(LRU))
- [Cache replacement policies - MRU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Most_Recently_Used_(MRU))
- [Cache replacement policies - LFU](https://en.wikipedia.org/wiki/Cache_replacement_policies#Least-Frequently_Used_(LFU))

## Requirements
### Python Scripts
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7.
- All files should end with a new line.
- The first line of all your files should be exactly `#!/usr/bin/env python3`.
- A `README.md` file, at the root of the folder of the project, is mandatory.
- Your code should use the `pycodestyle` style (version 2.5).
- All files must be executable.
- The length of your files will be tested using `wc`.
- All modules should have documentation.
- All classes should have documentation.
- All functions (inside and outside a class) should have documentation.
- Documentation should be a real sentence explaining the purpose of the module, class, or method.

## BaseCaching Parent Class
All your classes must inherit from the `BaseCaching` class defined below:

```python
#!/usr/bin/python3
""" BaseCaching module
"""

class BaseCaching():
    """ BaseCaching defines:
      - constants of your caching system
      - where your data are stored (in a dictionary)
    """
    MAX_ITEMS = 4

    def __init__(self):
        """ Initialize
        """
        self.cache_data = {}

    def print_cache(self):
        """ Print the cache
        """
        print("Current cache:")
        for key in sorted(self.cache_data.keys()):
            print("{}: {}".format(key, self.cache_data.get(key)))

    def put(self, key, item):
        """ Add an item in the cache
        """
        raise NotImplementedError("put must be implemented in your cache class")

    def get(self, key):
        """ Get an item by key
        """
        raise NotImplementedError("get must be implemented in your cache class")

