---
layout: post
title:  "Jupyter Notebooks vs Excel."
date:   2023-12-17 00:00:00 +0000
categories: general
tag: [engineering, python, software]
---

After spending several months with Visual Basic for Applications (VBA) within the MS Excel environment, I found myself at a crossroads. 
The efficiency VBA provided in automating tasks was undeniable; however, I was missing a more modern and flexible programming environment. 
The inability to code outside MS Office programs made VBA less and less attractive. I decided to research solutions that would still allow me to
easily interact with spreadsheet like data structures and have the capabilities of MS Excel while being more convenient for a person without a CS background.

Python programming language has a very strong position in the engineering environment as an approachable and pleasant to learn. Particularly enticing element
is the extensive number of libraries containing engineering calculations, which additionally simplifies the process of building automation of mechanical calculations.
Compared to VBA, which doesn't have nearly as active a community as python and access to the aforementioned libraries, made me decide to jump the VBA ship and dive into the python.

Next, I came across the <a href="https://jupyter.org/" target="_blank" rel="noopener">Jupyter</a> project. It's an open source
that revolves around the development of the Jupyter Notebooks. Web-based application that allows users to create and share documents combining live code, 
equations, plots, and regular text. Paired with Python, it is presented to be the perfect starting point to step away from Excel based VBA and still
work on engineering automation. 

# Jupyter Notebooks
To start with, Jupyter Notebooks have to be installed locally on your machine, after installing <a href="https://www.python.org/" target="_blank" rel="noopener">Python</a>. It can be installed
separately or as a bundle together with <a href="https://www.anaconda.com/download" target="_blank" rel="noopener">Anaconda</a> Distribution.k
Alternatively, you can install notebooks using pip (pyhon package manager), however, Anaconda provides libraries that will most likely be useful 
for writing any application that handles datasets. 

To launch the notebooks, you can run the Anaconda Navigator and select them there, or simply type `jupyter notebook` in terminal (the exact command may vary depending on your operating system).
This command will open up a web browser with jupyter dashboard of the currently opened directory. You can then navigate to the desired location and create a new notebook.
You can choose either python, markdown or regular text file, but the most interesting for now is a Notebook option.
This will open up a new window in your browser with an empty notebook asking you which kernel to choose, proceed with Python3.
Your browser should look as follows:

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2024-12-17-jupyter-notebooks/assets/empty-notebook.png?raw=true" width="640" height="248">
</center>

# Notebook Interface
The First thing you may have noticed is an input field in the middle of the screen. This is a cell. The Content of the cells may vary, but 
primarily there are two types of cells. One that contains python code, and the other that contains Markdown code. 
Python cells are where you write and execute your Python code. You can create a new code cell by clicking the "+" button in the toolbar or by pressing B (for "below") while in command mode (blue cell border).
To execute a code cell, press Shift + Enter. The result will be displayed below the cell.

Markdown cells are used for adding text explanations, documentation, or even LaTeX equations using Markdown syntax. 
You can create a new Markdown cell by clicking the "+" button in the toolbar and selecting "Markdown" from the dropdown menu.
You can render the Markdown text the same way as executing code in python cell, using Shift + Enter.
Markdown is a simple markup language that uses plain text-formatting syntax to create rich-text documents. It allows users to simply format  
and structure text using simple symbols. It is common among many text editors, and you can use it to a style text of readme file in your GitHub repository or
stackOverflow question. 

Combining those two features allows user to create nicely formatted templates that can be extremely useful even for people that 
are not programming literate. You can also insert images/videos and with LateX insert equations. 
Simple example shown below: 

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2024-12-17-jupyter-notebooks/assets/example-notebook.png?raw=true" width="640" height="248">
</center>

On top of that, a function that I personally found very handy, especially at the beginning of coding, is how cells are executed.
You can either execute all cells in the notebook at once, sequentially one after another from top to bottom, or each cell separately.
I consider it useful because often when I was working with an elaborate chain of calculations, I wanted to check 
intermediate values of certain variables to quickly verify if my code is working as intended.
Normally, I would need to debug the code and use breakpoints to find a line that causes issues. With notebooks, I could set up my project
in a way that every cell is responsible for a fundamental piece of code, and I can quickly verify the values as I am executing cell one by one.
Once I was ensured that everything works correctly, I merged the code into a single cell to have a nice and concise calculation.

# Version Control and Code storage
At first, it is not entirely clear where and how the notebooks are stored and saved. Effectively when running the notebooks from the terminal,
jupyter dashboard will show you the directory you executed the command from. And unless chosen otherwise, the newly created notebook (or different file)
will also be saved in the same location. What it means is that if you want to have your project synced between multiple devices, you can either save notebooks
in a directory that you will create a GitHub repository in, or save it in your DropBox directory. I would suggest using GitHub, because 
then you will be able to see every change in the notebook file, whether it's an addition, modification or removal. Also, it allows others 
to collaborate with you on the project if needed.

To store individual notebooks on GitHub, you would need to run git commands manually from the terminal. JupyterLab, however, has a git extension 
which makes the whole process even more pleasant and straightforward. JupyterLab will have a separate article coming in the following weeks, but essentially
it is an entire development environment. It offers more options in terms of managing notebooks, widgets and custom interactive components.

# Summary
Overall, I find Jupyter Notebooks to be a fantastic project, which may be a good first step for either someone who wants to start
programming for engineering/data science or someone who (like me) has come to the conclusion that VBA became unattractive.
The First steps in this project are relatively simple, since there is a massive community around notebooks and python in general.
Besides, this is also a great way to start familiarizing oneself with python, so further change to write standalone applications in 
full-blown IDE will be even easier.
