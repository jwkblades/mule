Mule, the stupid package manager
================================

Mule is a quick and easy package manager which allows you to create and manage repository mirrors easily. Inspired by git and vundle, mule aims to allow you the ease of accessing multiple repository mirrors with potentially differing packages, and is aimed at workplace environments where newhires need to get off the ground running but installing all the potentially needed (or wanted) software for the end user isn't always an option.

Setting Up A Mule Repo Mirror
=============================

Setting up a repo mirror is as easy as setting up a git server. Once you have your git server up simply start adding packages to it (view example.bag to see how packages are expected to be -- when we get them implemented).

Mule Commands
=============

install BAG
-----------
Install the specified BAG (package) on your machine if it is found and supports 
your OS.

remove BAG *(TODO)*
----------
Remove the specified BAG from your machine if it is installed.

update
------
Update all of the known repo mirrors and download any BAG updates which are 
available.

repo
----
Manipulate the repo mirrors which mule will look at.

repo add REPO
-------------
Add the specified REPO to the repos list (stored in the .mule file) if it 
doesn't already exist.

repo remove REPO
----------------
Remove the specified REPO from the repos list if it exists.

repo list
---------
List all REPOs in the .mule file

repo help
---------
Show the repo usage message.

File Formats
============

.mule
-----
A JSON object containing a repos member which is an object of name to REPO URL key-value pairings, and a bags member which is an array of bag objects (following the examples.bag model) that are installed on the machine.

example.bag
-----------
A JSON object containing name, version, description, keywords, author, 
dependencies, devDependencies, installer, uninstaller, and license members.

Requirements
============
perl, perl-JSON, git

License
=======

(The MIT License)

Copyright (c) 2013 James Blades &lt;jwkblades@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software, and 
that credit be given where credit is due.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
