Mohn Lab best practices for writing bioinformatics scripts
==========

**Overview**

Computers are powerful tools for researchers in the life sciences however, scientist are not usually trained in software development. Anyone who writes scientific software can benefit from following established best practices. Following these practices allow the researcher develop code that creates reproducible and scientifically sound results.

The following standards are strongly based on the articles below:

* Best Practices for Scientific Computing [\[doi:10.1371/journal.pbio.1001745\]](http://www.plosbiology.org/article/info%3Adoi%2F10.1371%2Fjournal.pbio.1001745)

* Ten Simple Rules for Reproducible Computational Research [\[doi:10.1371/journal.pcbi.1003285\]](http://www.ploscollections.org/article/browse/issue/info%3Adoi%2F10.1371%2Fissue.pcol.v03.i01)

* Ten Simple Rules for the Open Development of Scientific Software [\[doi:10.1371/journal.pcbi.1002802\]](http://www.ploscompbiol.org/article/info%3Adoi%2F10.1371%2Fjournal.pcbi.1002802)

**General Guidelines**

1. Write programs for people, not computers. 
    - Clarity should be emphasized. 
    - Use informative variable names, avoid using names of existing functions of variables (e.g. mean)
    - Variables should be nouns, functions should be verbs
    - Be consistent with indentation
    - Use informative comments, avoid in line comments
    - Separate names with underscores instead of dots (variable_1 Yes, variable.1 No). CamelCase is also OK.
    - Avoid long lines of codes, separate in multiple lines for clarity
    - Use meaningful file names and the correct extension (.r no, .R yes)
    - Surround these binary operators with whitespaces (=, ==, >=,<., ect )
    - Use spaces always after a comma, never before a comma. 
2. Do not "reinvent the wheel"
    - Check if others have come up with a verified, published solution to your problem before writing your own software.
3. Use standard packages instead of obscures ones, they are more likely to be tested and maintained
4.	Make incremental changes
    - When writing long codes, divide the task in smaller parts that can be performed by custom functions. Create these functions and, create and test them. It will make the whole process easier to debug.
5.	Plan for mistakes
    - Use assertion functions, and internal tests. Do not expect the user to give you the right input
    - Test your scripts with example data, and try to include positive and negative standards. Save the test files.
6.	Optimize software only after it works correctly
7.	Document design and purpose, not mechanics.
8.	Backup your data
9.	At minimum your raw data and the scripts used to generate the analysis results.

**Recommended style guides**

For Python code, [following PEP8 standard](http://legacy.python.org/dev/peps/pep-0008/) is recommended. For R we recommend that you follow [this standard.](http://stat405.had.co.nz/r-style.hml)

**Version Control**

One should create and use a [Github](https://github.com/) repository to store your working code and keep track of its modifications. A repository is helpful for reproducing past results and restoring functionality after drastic code changes. They are also essential if you are developing code as a team.

**R specific**

Save scripts and sessions. If revising old results, open a previously saved session instead of running the script again, this will save time and avoid changing your results if your script calls random numbers.

At the end of your scripts add the following lines to obtain the version of R you are using and the versions of the libraries used:
    - Version
    - sessionInfo()
    
Save this information as it will be import for others to know when you publish.

**Resources**

[Software carpentry](http://software-carpentry.org/index.html) has very clear and easy video tutorials on Unix, Python, and version control.

**Notepad++**

This Windows program is very useful to edit codes because it will tell you visually using colors if you have errors in indentation and closing brackets/parenthesis/brace. Download it [here](http://www.notepad-plus-plus.org/).
