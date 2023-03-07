---
title: What's the process of fetching JSON from a webpage to a Python script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the requests library in Python to send an HTTP GET request to the webpage URL, and then use the json() method on the response object to get the JSON data as a dictionary.
---

**Contents**

[TOC]

# Section 1: Introduction

Web APIs and data feeds have revolutionized the way we access and use web data. When it comes to working with web data in Python, the JSON data format remains an excellent choice for lightweight data exchange. Python provides several built-in modules to work with JSON data. In this article, we'll explore how to get JSON data from a webpage into a Python script.

# Section 2: Using Requests library to Retrieve JSON Data

One popular Python library for making HTTP requests is Requests, which makes it easy to send HTTP/1.1 requests. To use the Requests library, first, we need to install it using pip.

```python
pip install requests
```

Once installed, we can use the library's `get()` method to retrieve data from a webpage. The `get()` method returns an instance of `Response`, which contains the server's response to our request. The `Response` object's `text` attribute is a string representation of the response's content. We can use the built-in `json` module to parse the response content as JSON data.

```python
import requests
import json

response = requests.get('https://example.com/api/data')
data = json.loads(response.text)
print(data)
```

In the above code, we use the `requests` library to retrieve data from the URL 'https://example.com/api/data'. We then parse the response's content as JSON using the `json.loads()` method and store the resulting data in a variable named `data`.

# Section 3: Using urllib library to Retrieve JSON Data

Python's built-in `urllib` module provides a simple interface for making HTTP requests. To use `urllib`, we can use the `urllib.request.urlopen()` function to make an HTTP GET request and retrieve data from the specified URL.

```python
import urllib.request
import json

response = urllib.request.urlopen('https://example.com/api/data')
data = json.loads(response.read().decode('utf-8'))
print(data)
```

In the above code, we use the `urllib.request.urlopen()` function to retrieve data from the URL 'https://example.com/api/data'. We then parse the response's content as JSON using the `json.loads()` method and store the resulting data in a variable named `data`.

Note: We need to decode the response's content to convert it to a string and then parse it as JSON data.

# Section 4: Using Selenium library to Retrieve JSON Data

Sometimes, we may need to retrieve JSON data dynamically generated by a webpage that relies on JavaScript to load or update its content. In such cases, we can use the `Selenium` library to automate browser interactions and retrieve the JSON data after it has been loaded.

```python
from selenium import webdriver
import json

driver = webdriver.Chrome() # Replace with appropriate webdriver
driver.get('https://example.com/api/data')
data = json.loads(driver.find_element_by_tag_name('pre').text)
print(data)
driver.quit()
```

In the above code, we use the `Selenium` library to automate a Chrome browser session and load the URL 'https://example.com/api/data'. After the page has been loaded, we fetch the JSON data using the `find_element_by_tag_name()` method and parsing the returned element's text using the `json.loads()` method.

Note: We need to have the appropriate webdriver installed and in the system path. For instance, for Chrome, we need to install the ChromeDriver and add it to the system path before running the code above.