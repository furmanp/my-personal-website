---
layout: post
title:  "Jupyter Notebooks vs Excel."
date:   2023-12-17 00:00:00 +0000
categories: general
tag: [engineering, python, software]
---

After spending several months with Visual Basic for Applications (VBA) within the MS Excel environment, I found myself at a crossroads. 
The efficiency VBA provided in automating tasks was undeniable, however I was missing a more modern and flexible programming environment. 
The inability to code outside MS Office programs made VBA less and less attractive and I decided to research solutions that would still allow me to
easily interact with spreadsheet like data structures and having the capabilities of MS Excel while being more convenient for a person without a CS background.

Python programming language has a very strong position in engineering environment as an approachable and pleasant to learn. Particularly enticing element
is the extensive number of libraries containing engineering calculations, which additionally simplifies the process of building automation of mechanical calculations.
Compared to VBA which doesn't have nearly as active community as python and access to aforementioned libraries made me decide to jump the VBA ship and dive into the python.

Next, I came across the <a href="https://jupyter.org/" target="_blank" rel="noopener">Jupyter</a> project. It's an open source
that revolves around the development of the Jupyter Notebooks. Web based application that allows users to create and share documents combining live code, 
equations, plots, and regular text. Paired with Python it presented to be the perfect starting point to step away from Excel based VBA and still
work on engineering automation. 

# Jupyter Notebooks
To start with, Jupyter Notebooks have to installed locally on your machine, after installing <a href="https://www.python.org/" target="_blank" rel="noopener">Python</a>. It can be installed
separately or as a bundle together with <a href="https://www.anaconda.com/download" target="_blank" rel="noopener">Anaconda</a> Distribution.
Alternatively, you can install notebooks using pip (pyhon package manager), however Anaconda provides libraries that will most likely be useful 
for writing any application that handles datasets. 

To launch the notebooks, you can run the Anaconda Navigator and select them there, or simply type `jupyter notebook` in terminal (the exact command may vary depending on your operating system).
This command will open up a web browser with jupyter dashboard of the currently opened directory. You can then navigate to desired location and create a new notebook.
You can choose either python, markdown or regular text file, but the most interesting for now is a Notebook option.
This will open up a new window in your browser with an empty notebook asking you which kernel to choose, proceed with Python3.
Your browser should look as follows:

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2024-12-17-jupyter-notebooks/assets/empty-notebook.png?raw=true" width="220" height="248">
</center>

## Notebook Interface
First thing you may have noticed is an input field in the middle of the screen. This is a cell. Content of the cells may vary, but 
primarily there are two type of cells. One that contains python code, and the other that contains markdown code. 
Python cells are where you write and execute your Python code. You can create a new code cell by clicking the "+" button in the toolbar or by pressing B (for "below") while in command mode (blue cell border).
To execute a code cell, press Shift + Enter. The result will be displayed below the cell.

Markdown cells are used for adding text explanations, documentation, or even LaTeX equations using Markdown syntax. 
You can create a new Markdown cell by clicking the "+" button in the toolbar and selecting "Markdown" from the dropdown menu.
You can render the Markdown text same way as executing code in python cell, using Shift + Enter.

