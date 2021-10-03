---
layout: post
title:  "Run LINUX Command in Windows"
date:   2021-09-08 17:01:52 +0800
categories: jekyll update
category: tut
image: /assets/images/info.png
image2: /assets/images/drives.png
image3: /assets/images/org_file.png
image4: /assets/images/file_created.png
image5: /assets/images/sample.png
image6: /assets/images/window.png
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

grep a file to generate text file

The original file:
![grep file]({{ page.image3 | relative_url }})

```
grep -i bianca movie_lines.txt > bianca.txt
head bianca.txt
```
![grep file]({{ page.image4 | relative_url }})

Sample of output file
![grep file]({{ page.image5 | relative_url }})

The file is also created in windows folder
![grep file]({{ page.image6 | relative_url }})

Another powerful technique is running shell scripts in windows using bat file.
1. Define your local mobaxterm_path environment variable 
2. Call mobaxterm and use its interface to run
3. Run .sh
4. Close the mobaxterm.exe when finishing

```
@ECHO OFF
SET mobaxterm_path_sh=D:\MobaXterm_Portable_v21.3\MobaXterm_Personal_21.3.exe
SET win_path=D:\Programming_practise\sh
call %mobaxterm_path_sh% -newtab -exec "cd /drives/d/Programming_practise/sh; sh test.sh" -exitwhendone
```

sh file content
```
grep

sed
```


Close the mobaxterm.exe when finishing
```
MobaXterm.exe -exitwhendone
```
For more, read [documentation](https://mobaxterm.mobatek.net/documentation.html#5_4) in section 5.4 
