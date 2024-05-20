---
layout: post
title:  "Marine Operations Toolbox."
date:   2024-05-20 00:00:00 +0000
categories: general
tag: [engineering, web, software]
---

I'm excited to finally share a project I've been working on since joining my new company as a 
Software Engineer. This web-based tool, the
<a href="https://twd.nl/marine-operations-toolbox/" target="_blank" rel="noopener">Marine Operations Toolbox</a>. Since it 
aligns perfectly with the focus of this blog I have decided to write here about it. <br>
It aims to simplify and semi-automate various engineering tasks, specifically 
supporting marine engineers with pre-operational tasks. <br>

Currently, the toolbox includes five applications Deck Layout, Bollard Pull, Spreader Beam, Barge Stability and Monopile 
operations. I want here to focus primarily the Deck Layout app, 
as I was involved with the most. 

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/master/_posts/2024-05-20-marine-operations-toolbox/assets/MOT.png">
</center><br>

# motivation 

The primary motivation behind creating this tool stemmed from the frequent requests our company receives to design sea 
fastening for various objects and machinery on vessels. 
Typically, this process starts with providing a preliminary workability drawing alongside the 
proposal. This drawing serves as an initial analysis, outlining the positioning of operational equipment 
on the vessel's deck, considering any existing obstructions and deck reinforcements. 

Since these drawings are produced during the tender process, they are often rudimentary and 
serve as a high-level overview rather than a comprehensive technical document.

The task comes down to analyzing vessel 2D drawings in AutoCAD, where the draftsman positions top, 
side, and aft/front projections of the equipment intended for sea fastening on the deck. 
The objective is to ensure there are no collisions and that the items are roughly aligned with 
the underlying structure. 

Our approach to this challenge was twofold. Firstly, salespersons are typically not experienced in 
running such analyses and often lack the available time to do so. 
Secondly, engineering teams are frequently occupied with ongoing projects, 
making it challenging to address these tasks promptly, thereby prolonging the tender 
process and potentially jeopardizing signing the  project for the company.

# solution

Our proposal aimed to simplify, gamify even, the process by transitioning it to a web browser
platform. This approach would significantly reduce the barrier to entry for conducting the analysis, 
eliminating the requirement of proficiency in AutoCAD; software often perceived as complex. 
This shift would allow salespersons to undertake the task with ease.

Moreover, recognizing the limited number of vessels and equipment utilized in our industry, 
we opted to aggregate and serialize all relevant models. 
By making these models accessible within the application, we could decrease even further the process of 
generating and releasing the necessary documents.

# implementation

Despite many engineering applications being built in Python, Deck Layout is built using Node.JS with 
Express.js running the backend and handling React the frontend.
However, what is particularly interesting about this project is the use of products that enable viewing and interaction
with .dwg drawings through a web browser.

The .dwg format is a widely-used file format for storing two and three-dimensional design data and 
metadata. Developed by Autodesk, it is the native format for AutoCAD files.
The .dwg format supports a range of data types, including vector graphics, text, 
and embedded metadata, making it a standard in the engineering, architecture, and construction 
industries. This format however is troublesome when it comes to display and interact with it online. 

Recently, Autodesk released a new product called 
<a href="https://aps.autodesk.com/" target="_blank" rel="noopener">Autodesk Platform Services</a>.
This development platform includes a set of APIs that allow developers to interact with selected Autodesk products. 
One of these is the <b>Autodesk Viewer</b>, an online engine that enables users to display and interact with .dwg 
files that have been converted (using another APS API) to a web-suitable format.

Since the Viewer has also a SDK available, we have built numerous functionalities around it,
allowing users to aggregate, position, rotate, and scale the drawings. Utilizing the power of the .dwg format,
models not only hold geometrical data but also additional information about their physical properties,
which can be used to further simplify calculations.

To improve user experience, features like dragging models with the mouse pointer or using arrow keys make
the process much simpler compared to AutoCAD. While this tool provides only a fraction of AutoCAD's functionality,
most of the advanced features are unnecessary for this purpose, making the layout tool fit for its intended use.

Additionally, once the layout is complete, users can generate and download a .dwg drawing of their design using
the layout tool. This capability is enabled by another API from Autodesk Platform Services.

# summary

Above functionality, combined with approachable controls and centralized data for equipment models and vessels, 
makes the process of creating workability drawings much simpler and faster. By storing commonly used equipment and 
vessels within the app, providing simple and intuitive controls for manipulating the models, and allowing users 
to generate the drawing on the spot, the time required to produce a workability drawing is significantly reduced. 
Additionally, there is no need for advanced AutoCAD skills or a license, as the APIs are paid per use.
I am quite happy with the product, especially considering the feedback we had received and I hope we will continue 
further development.

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/master/_posts/2024-05-20-marine-operations-toolbox/assets/layout-app.png">
</center>
<br>
