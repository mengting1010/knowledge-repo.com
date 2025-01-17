---
title: The plot displayed by plt.show shows the entire graph, but when using savefig, the image gets cut off
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Savefig uses the default DPI value of 100, which can cause the image to be cropped if the figure size is not adjusted properly.
---

**Contents**

[TOC]

Section 1: Introduction
When we visualize graphs or plots of data in Python, we often use the Matplotlib library. Matplotlib provides various saving options to save the graph or plot as an image file. However, sometimes the saved image might be cropped, even though the full graph is visible in the figure window generated by plt.show() method.

Section 2: Understanding the issue
The issue of cropping occurs because Matplotlib needs to determine the size of the figure before saving it. This process is based on the parameters set in the backend that we are using. For example, the default backend in Matplotlib is 'Agg' that uses a DPI (dot per inch) of 100. If the size of the figure is larger than the set DPI, then it will be cropped while saving the image.

Section 3: Solutions to the issue
There are several solutions to this issue, which include:

a) Change backend: One of the easiest solutions is to switch to a different backend that supports higher DPI. For example, we can switch to the 'pdf' backend using the following command:
    ```python
    import matplotlib
    matplotlib.use('pdf')
    ```

b) Change DPI: We can also change the DPI to a higher value so that the saved image is not cropped. For example, we can set DPI to 300 using the following command:
    ```python
    plt.savefig('filename.png', dpi=300)
    ```

c) Adjust figure size: Another solution is to adjust the size of the figure so that it fits within the set DPI. We can do this by setting the figsize parameter in Matplotlib, as follows:
    ```python
    plt.figure(figsize=(8,6))
    plt.plot(x,y)
    plt.savefig('filename.png')
    ```

Section 4: Conclusion
In conclusion, when we use plt.show() to visualize graphs or plots in Python, the saved image might be cropped if the size of the figure is larger than the set DPI. We can overcome this issue by changing the backend, adjusting the DPI, or adjusting the figure size. By implementing these solutions, we can ensure that the saved image contains the full graph without any cropping.
