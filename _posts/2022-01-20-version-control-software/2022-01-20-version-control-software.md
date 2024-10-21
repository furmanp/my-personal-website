---
layout: post
title: "version control software."
date: 2022-01-20 00:00:00 +0000
categories: general
tag: [ visual basic, documentation, version control ]
---

When developing a script with Visual Basic, most likely you are using built-in IDE
`(Integrated Development Environment)`, meaning
you either go to Visual Basic Editor through the Developer tab in Excel or simply press `alt + F11`. Although the editor
is simple, it has most
of the functionalities you may need, except for one problem - you have to open an Excel spreadsheet first, meaning you
cannot access
the code only. It does not cause any critical issues or inconveniences unless you want to collaborate on development
with someone else but you,
or you want to control changes in your code. It means that if you or anyone else in the team makes an update that does
not
entirely follow your initial objectives, you will have a bad time finding the bug unless you create new spreadsheets
prior to any updates
you want to introduce.<br>
Unfortunately, VBE does not provide an in-house solution for that. This article describes a solution I have found and
used for some time now.
Despite having some flaws, it is serving its purpose and helped to push forward my cooperation with the team on the
development our
Visual Basic projects.

# enhance your VBE

First, you will need to get <a href="https://rubberduckvba.wordpress.com/" target="_blank" rel="noopener">Rubberduck</a>
extension.
It is an open source add-in for Visual Basic having plenty of useful functions, however, in this article, I want to
focus on a particular one
that is necessary to have the entire setup working smooth and sound.

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2022-01-20-version-control-software/assets/rubberduck_logo.png?raw=true" width="220" height="248">
</center>

Rubberduck is essential in the process because when exporting modules as binary files directly from VBE, there are no
`Atributte` values
written to the .bas file. Those values, in short, provide the information which particular part of the code was modified
and presents it to
you when committing changes. So in the end, without those values, you cannot track changes you have made along the way,
which is actually
a point of this topic.<br>
Thr second feature, being less necessary but also helpful is that you can export an entire folder at once, rather than
module after module which
maybe painstaking.

I highly recommend diving in and trying other features of Rubberduck. Even though they are not essential to the
described process of VCS, they are
still extremely useful and ~~can~~ will make the whole process of development more pleasant.

# foundation is ready, time to commit

The system I intend to describe in the following paragraph is called `Git`. It is a system for tracking changes in any
set of binary files.
Created by Linus Tornvalds in 2005, currently available from different providers as being broadly used in the software
development industry.
Personally, I use <a href="https://github.com/" target="_blank" rel="noopener">Github</a>. It is extremely easy to use
with nice and clean
desktop interface which allowed me to understand the entire process better without having to use terminal commands from
the very beginning.

The structure of the workflow looks as follows; to store your data within Github, you need to create repositories. The
repository is a catalogue that will store data of your project and
for most of the time you will have one repository per project. This repository should store the newest version of your
project files.
Prior you start updating your project you should first update it - `pull`, and when finished `commit` to save and `push`
to put the new version online.
The picture below clearly presents the workflow.

<center>
<img src="https://github.com/furmanp/my-personal-website/blob/master/_posts/2022-01-20-version-control-software/assets/workflow_chart.png?raw=true" width="600" height="386">
</center>

If you made changes in the project you are unsure of, you can create a branch that stores your updated version
separately from the main structure
of the project until you test it and verify that everything is ok. Once that is done, you can simply merge with the main
branch, so it is up-to-date. The additional branch can be deleted, but not necessarily.

This briefly sums up the essentials of the process which is required to have it up and running.
However, Github has much more to offer, and despite being a user for a couple of months now I am far from using its full
capabilities and yet it still helped
me a lot with managing project files. Thus I will not explain in detail what and how you can work with it, rather I will
highly recommend visiting
<a href="https://docs.github.com/en/get-started" target="_blank" rel="noopener">this website</a> where the entire
process of creating your first
repository, branch, making a commit etc. are carefully explained - definitely better than I would ever can.
