---
layout: post
title:  "Run LINUX Command in Windows"
date:   2021-09-08 17:01:52 +0800
categories: jekyll update
category: tut
image: /assets/images/info.png
image2: /assets/images/drives.png
---

If you are experienced in using the LINUX command to grep unique words from large files, you’d love those amazing tools and wonder why windows do not have such a command in MS-DOS. Then, using Mobaxterm in Windows is a good choice.

I had a task to paste numerous lists in the Windows platform which should have the result of using the LINUX command, grep and sed, in some files. I tried to use it in Python. Yes, it is successfully running but the O(n) is very large and time-consuming. I was inspired by my colleagues. He showed me how to use git bash and Mobaxterm run in Windows by typing the LINUX command. Wow, it motivated me to keep researching the hidden function in Mobaxterm.

The latest version of Mobaxterm is [v21.3](https://mobaxterm.mobatek.net/download-home-edition.html). You can download portable or installers up to your environment.

This is your local terminal and you can start to run UNIX tools
![MobaXterm]({{ page.image | relative_url }})

If you need to change to other drives:
```
cd /drives
```
![grep file]({{ page.image2 | relative_url }})

grep a file to generate text
```
grep -i bianca movie_lines.txt > bianca.txt
```


use batch file to call Mobaxterm

create tab
Another powerful technique is running shell scripts in windows using bat file.

run sh
call mobaxterm and use its interface to run

For more, read documentation
