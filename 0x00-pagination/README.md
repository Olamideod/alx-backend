# Pagination Project

This project involves implementing pagination for a dataset of popular baby names. The goal is to learn how to paginate a dataset with simple page and page_size parameters, with hypermedia metadata, and in a deletion-resilient manner.

## Learning Objectives

By the end of this project, you should be able to explain:

- How to paginate a dataset with simple page and page_size parameters
- How to paginate a dataset with hypermedia metadata
- How to paginate in a deletion-resilient manner

## Requirements

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- A `README.md` file at the root of the folder of the project is mandatory
- Your code should use the pycodestyle style (version 2.5.*)
- The length of your files will be tested using `wc`
- All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- A documentation is not a simple word; it’s a real sentence explaining the purpose of the module, class, or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated

## Setup

Download the `Popular_Baby_N
# Pagination Project

This project involves implementing pagination for a dataset of popular baby names. The goal is to learn how to paginate a dataset with simple page and page_size parameters, with hypermedia metadata, and in a deletion-resilient manner.

## Learning Objectives

By the end of this project, you should be able to explain:

- How to paginate a dataset with simple page and page_size parameters
- How to paginate a dataset with hypermedia metadata
- How to paginate in a deletion-resilient manner

## Requirements

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- A `README.md` file at the root of the folder of the project is mandatory
- Your code should use the pycodestyle style (version 2.5.*)
- The length of your files will be tested using `wc`
- All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- A documentation is not a simple word; it’s a real sentence explaining the purpose of the module, class, or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated

## Setup

Download the `Popular_Baby_Names.csv` file and place it in your project directory. This dataset will be used for the project tasks.

## Tasks

### 0. Simple helper function

Write a function named `index_range` that takes two integer arguments `page` and `page_size`. The function should return a tuple of size two containing a start index and an end index corresponding to the range of indexes to return in a list for those particular pagination parameters. Page numbers are 1-indexed.

### 1. Simple pagination

Implement the `Server` class to paginate a database of popular baby names. The class should include a `get_page` method that takes two integer arguments `page` (default value 1) and `page_size` (default value 10). Use the `index_range` function to find the correct indexes to paginate the dataset correctly and return the appropriate page of the dataset.

### 2. Hypermedia pagination

Implement a `get_hyper` method in the `Server` class that takes the same arguments as `get_page` and returns a dictionary containing the following key-value pairs:
- `page_size`: the length of the returned dataset page
- `page`: the current page number
- `data`: the dataset page
- `next_page`: number of the next page, `None` if no next page
- `prev_page`: number of the previous page, `None` if no previous page
- `total_pages`: the total number of pages in the dataset

### 3. Deletion-resilient hypermedia pagination

Implement a `get_hyper_index` method in the `Server` class that ensures the user does not miss items from the dataset when changing pages, even if certain rows are removed between queries. The method should return a dictionary with the following key-value pairs:
- `index`: the current start index of the return page
- `next_index`: the next index to query with
- `page_size`: the current page size
- `data`: the actual page of the dataset

## Running the Tests

To run the provided test files, use the following commands:
```bash
./0-main.py
./1-main.py
./2-main.py
./3-main.py

## Author 

Olamide David Oluwamusiwa

