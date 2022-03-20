---
layout: post
title:  "development of prototype element using vacuum bag only technology."
date:   2022-03-20 00:00:00 +0000
categories: general
tag: [composites, prototyping, vacuum bag only, prepreg]
---
The following project was to deliver prototype series of orthopedic ankle protectors, considering that the process should mimic serial production. 
The technology used for development should be as close as possible to the one that will be used in serial production and will allow for a certain level of optimization keeping properties of the product intact.
The prototypes were aimed to present the product's final look along with its mechanical properties, surface finish, and overall feeling of the product. 

# initial analysis

Taking into account limitations caused by the material that was to be used (carbon fibre), the initial phase of the project was focused on analyzing the manufacturability of the elements, 
which impacts the technology used to produce the parts along with mechanical properties. Considering the fact, that many elements are quite often designed by designers, 
focusing mostly on the visual aspect of the project, the role of the design engineer is to propose a solution that will not affect the visuals of the product, 
ensuring that its mechanical properties fulfil initial boundary conditions and allow manufacturing of them as easy as they possibly can. Obviously, 
selected technology will highly affect the final price of the product, however detailed analysis should be done in cases like that, as the price may not be the driving factor. 
In this project, analysis has been finalized after the second iteration. The picture below presents the initial version of the described parts. The entire protector consists of two main elements; 
the bottom one holding a foot in an upright position and the top, necessary to stabilize the upper area of the ankle. The remaining elements have been excluded from the analysis due to low structural importance.

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-1.png">
</center><br>


Considering boundary conditions of the project (perspective of high-volume production) technologies that are labour-intensive were not taken into account. 
The main methods that fit into customers’ business cases were hot compression moulding, vacuum bag only/out of autoclave, resin transfer moulding, autoclave.
The geometry that has been presented in the prior picture shows, that compression moulding has to be ruled out as it is either impossible to manufacture, 
or the tooling cost would highly exceed the budget due to shape complexity. Both bottom and top pieces of the mould would need to consist of more than 2 parts and additionally be 
equipped with mechatronics actuators to allow evenly distributed pressure and proper mould closure. The situation looks similarly considering resin transfer moulding. 
If the amount of elements that are to be manufactured would have been significant, the cost of tooling would not make big difference. However, at this stage of the project, 
the focus was placed on quality rather quantity, as this was to be the first batch of prototypes.
The remaining two technologies from the four that had been previously mentioned are rather similar. 
Both require building a layup on a single pieced, male type mould, which is wrapped with an airtight bag and have the air sucked out, creating a vacuum inside. 
Further on, the package can be placed either in an autoclave or in a regular oven. Autoclaves can provide additional pressure outside the bag and heat, whereas ovens provide just heat, 
what is the main difference between these two technologies. Despite the fact, that autoclave technology provides superior quality, it also increases the cost of the final product. 
Thus, after analysis, it has been concluded that VBO (Vacuum Bag Only) technology will be sufficient and has been chosen to proceed with. 
Although the technology has been selected, simplification of the top part of the element was recommended. The second image presents a later version of the element, 
where certain alterations have been made. The top piece of the element was split into two identical elements and removing the front part, as it did not play any 
significant role in the element considering its degrees of freedom. 

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-2.png">
</center><br>


The way that elements are constrained between each other shows that forward and backward movement is allowed, hence there is no clear reason why the top piece should have extra material in the front area. 
Even after removing that part, the element will still provide sufficient support in a sideways direction, which is the main goal of this product.
The image below precisely shows the designed degrees of freedom. 

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-3.png">
</center><br>


Alterations that were introduced also highly simplify the manufacturing process, as the top pieces are identical which is extremely beneficial in terms of serial production.
Once the design has been fixed, a matrix of configurations was defined to see how different layups will affect the behaviour of the product. 

# tooling

Once the design of the elements was fixed, the team could proceed to design the tooling. Because the technology had been fixed as well and it is a prototyping stage tooling was rather simple. 
However, a list of conditions had to be fulfilled to get the required quality of the element and these are surface finish, heat capacity, compression strength, porosity. 
For the described project, compression strength was not relevant as the maximum possible pressure is 1 bar due to vacuum pressure. 
Currently, the market offers many different tooling resins sold in blocks, which are easily machined and give good looking results, 
but they often are quite porous and require an extra amount of work to get the surface nicely finished.
Thus again, despite this being a prototyping series, certain conditions had to be considered like for serial production. If the mould surface was not good enough, 
it would transfer the defect to the product. The customer required the surface to be smooth and shiny, hence tooling was made from aluminium. With relatively low effort, good quality has been achieved.

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-4.png">
</center><br>

# manufacturing 

To provide the best representation of the final product and limit post-processing before the manufacturing flat patterns have been created. 
A flat pattern is a 2D representation of a 3D shape. It has a certain error, but it is the best way to minimize waste of raw materials and limit post-processing time. 
The aforementioned patterns were cut using a CNC plotter. 
Another important thing is corner compensation on the further plies. As the layup is being built, the radius in the corner changes due to single ply thickness. 
This fact should not be avoided when building an element from numerous plies. This means that the first ply to the mould will be shorter in certain directions, compared to the last one. 
The picture below shows one of the flat patterns used in the project. The hole in the middle was cut to provide accurate positioning ply on the mould.

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-5.png">
</center><br>

Secondly, composites have isotropic mechanical properties, the angular position of the flat pattern matters because different fibre angles may result in different properties in the final product. 
Finally, a note on the fabric weave should be taken. Not all of the weaves are suitable for curved surfaces – this effect is called drapability and it is important to take that into account when designing layup of the elements. 

Before working with prepregs, two important things should be mentioned. First, quite obvious but may be easily overlooked is that prepregs usually have a resin-rich side. It is recommended to place prepregs facing the resin-rich side towards the mould surface.
Next thing is, that prepregs are stored at low temperatures to prevent the resin from curing. To provide a better manufacturing experience is best to warm up the material and moulds to room temperature. This will make the prepregs tacky and they will stick to the mould nicely. 
Setting mechanical properties aside, some carbon fibre elements are also expected to look good. Thus, it is important to be careful and gentle when laying up the plies, not to dislocate the fibres.

After the first play is done, it is recommended to run a process called debulking. It is a process to get rid of all the air that may have been enclosed between the first ply and the mould surface. This is extremely useful because it highlights spots where bridging occurs. It is made by closing the mould with the first ply in the vacuum bag and applying vacuum for roughly 15 minutes. Studies have shown that a long time does not have an impact on the result, shorter however does. Afterwards, the next plies can be placed on the mould. Depending on the number of the plies, and the overall thickness of the element, debulking should be made a couple of times, once per 2-3 plies. Although this process is time-consuming, it highly increases the quality of the product. 

<br>
<center>
<img src="https://raw.githubusercontent.com/furmanp/my-personal-website/6b45c1c80cd0e60d29031cbaa3f3412a06e61a56/_posts/2022-03-21-composite-element-using-VBO/assets/image-6.jpg">
</center><br>

Once layup is done, the entire element should be wrapped in the vacuum bag once again, with the air sucked out. The bag has to be completely airtight, otherwise, 
pressure may be insufficient for proper consolidation of the composite. 
It is recommended to insert a thermocouple inside the bag, to make sure that the temperature of the composite element is sufficient for the complete curing of the resin. 
Prepregs datasheet usually stores all required information about the temperature profile that is required to achieve the full cure of the resin.

# summary 

VBO technology provides good results, however, is time-consuming and requires a certain level of manual skills. Although It is not suitable for high volume production, 
it allows the creation of a small to moderate series of prototypes for a relatively low cost compared to other methods. Quality-wise, elements were looking according to specifications, both visually and mechanically. 
In terms of process effectiveness, it can be placed in the middle of the ladder. Manual layup is quite intensive, but using prepregs instead of running an infusion saves a considerable amount of time. 
