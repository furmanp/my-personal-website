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

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2022-02-15-how-to-document-vba/assets/mkdocs.png?raw=true" width="572" height="341">
</center>

Once you are done with that, and you have created a new project, navigate in the terminal into the main directory where `mkdocs.yml` is located and type in command line `mkdocs serve`, 
this command will build your project and host it locally on your computer. The script will run in the background as long as you close or terminate it refreshing your code after each modification, 
so you can view how the website would look in its final form.

Due to the fact that `mkdocs` is really well documented I am not going to explain any further how to build and style your documentation. At the moment of writing this article, 
I am in the middle of developing my first project based on this framework and had no major problems with having it up and running, thus I do not expect that you will have either.

Once everything is done, and your website is complete, you have to generate the html output and deploy the website. 
To do so, while being in your project directory, type in the command line ``mkdocs build``. If everything goes well you can now deploy the project by typing `mkdocs gh-deploy`.
This command builds the aforementioned static html page and creates separate branch, `gh-pages`, where it stores all the necessary files.<br>
You are ready to publish your website now.

Keep in mind that after you made changes in content of your website, add a post or change anything in configuration files you have to rebuild the website and deploy it to your GitHub account,
so repository is up-to-date. In the near future I intend to create GitHub action for my documentation, so after the changes are commit and pushed to the repository, building and deployment will be done automatically.
Once I have it working I will describe the process in here as well.

# github pages

Let us head to the part, where your online documentation becomes literally online- hosting.
GitHub has an extremely useful feature that allows you to connect your repository to a custom domain. What it means is, 
you do not need to buy a domain or get a hosting plan for your website. Everything will be managed through GitHub with no costs involved. 
Unless you want to have a custom domain, then you can simply get one and connect it to GitHub pages.  There is one caveat though, your repository has 
to be public unless you are using paid GitHub plan.

To set it up, head to settings of the repository you want to publish, and select pages on the left-hand sight of the screen.
<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2022-02-15-how-to-document-vba/assets/gh_pages.png?raw=true">
</center><br>

Next, you need to choose which branch you want the pages to connect to, and a directory where your `index.html` file is located. 
If you leave the latter empty it will by default assume that ``root`` is the main directory. Click `Save` when done. 
    
<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2022-02-15-how-to-document-vba/assets/gh_settings.png?raw=true">
</center>
<br>

Url address of your website will be generated from your GitHub username, and repository name `http(s)://<username>.github.io/<repository>`.

Keep in mind that GitHub Pages is not intended for or allowed to be used as a free web hosting service to run your online business, e-commerce site, 
or any other website that is primarily directed at either facilitating commercial transactions or providing commercial software as a 
service. GitHub Pages sites shouldn't be used for sensitive transactions like sending passwords or credit card numbers.

For more detailed information you can look at <a href="https://docs.github.com/en/pages" target="_blank" rel="noopener">Github pages documentation.</a>

That pretty much sums up the entire process of establishing a website you can use to document the project. Being fully aware that this article is not so detailed
manual, I hope it gives clear overview what and how it should be done to succeed. 
