#Summary of the Data Scientist`s Toolbox course

This file contains a summary of the coursera course _Data Scientist`s Toolbox_
It contains info on:

* Getting help
* Other courses in the Data Science Specialization
* Command Line Interface
* Git Syntax
* Github Syntax
* Markdown Syntax
* Installing R packages

## Getting help
First look at the documentation and/or google your question. 
Then post questions on the message board, others can vote and answer your question.

**If you figure out the answer to a question on the forum, post the solution!**

R help functions:

* `?functionName` Access help file of _functionName_
* `help.search("functionName")` Search help file of _functionName_
* `args("functionName")` Get arguments (input/output) of _functionName_
* `functionName` See code of _functionName_

An R reference card can be found at "http://cran.r-project.org/doc/contrib/Short-refcard.pdf"

### Asking an R question
When asking an R question, think about:

* What steps will reproduce the problem?
* What is the expected output?
* What do you see instead?
* What version of the product (+packages) are you using?
* What operating system are you using?

Question title: PRODUCT VERSION + FUNCTION + OS + error

### Asking a data analysis question
When asking a data analysis question, think about:

* What is the question you are trying to answer?
* What steps/tools did you use to answer it?
* What did you expected to see?
* What do you see instead?
* What other solutions have you thought about?

Question title: METHOD + QUESTION TRYING TO ANSWER + IDEA FOR SOLUTION

### Where to find answers
R programming:

* Archive of the class fora
* Manual/help files
* Google (eg. [data type] R package)
* Ask skilled friend
* Class fora
* Post to R mailing list or Stackoverflow (use the tag "[r]")

Data Analysis/Statistic:
* Archive of the class fora
* Google / Stackoverflow (eg. [data type] data analysis)
* Ask skilled friend
* Class fora


## Other courses in the Data Science Specialization
TODO

## Command Line Interface
Tool which can navigate folders, create and edit files/folders/programs, run programs
A CLI command is of the form **command flags arguments**, the command is a task that should
be performed, the flags are options (always preceded by a `-`) and the arguments can be what is
modified or other options.

CLI commands:

* `pwd` print working directory
* `clear` clear CLI window
* `ls` list files and folders in the current directory
  - `-a` also show hidden files and folders
  - `-l` show details (combined flag = `-al`)
* `cd` change directory
  - no argument, go to home directory
  - path to directory, go the specified path
  - `..` go one directory up
* `mkdir` make directory, argument: name of the directory
* `touch` create empty file, argument: name of the file
* `cp` copy, argument 1: filename/directory name, argument 2: path to copy to
  - `-r` copy contents of a directory
* `rm` remove, argument: file to remove (**!Cannot undo a remove command!**)
  - `r` folder to remove
* `mv` move, argument 1: filename, argument 2: path to move to
  - When the second argument is just a name, the file is renamed
* `echo` print argument
* `date` print current date and time


## Git Syntax
Git is a version control system, 
this system records changes to a file or set of files over time 
so that you can recall specific versions later.

Git commands (always precede with `git `):

* `help`       display help index and most commonly used git commands
* `help <command>` display help for a specific command
* `config --global user.name "<username>"` set/update username
* `config --global user.email "<yourmail>"` set/update email
* `config --list` confirm changes to the config file
* `add`        Add file contents to the index
  - `.` adds all new files
  - `-u` updates tracking for changed/deleted files
  - `-A` does both of the previous
* `bisect`     Find by binary search the change that introduced a bug
* `branch`     List, create, or delete branches (also shows which branch you are on)
* `checkout`   Checkout a branch or paths to the working tree
  -`b branchname` create a new branch with the name `branchname`
  -`master`    switch back to master branch
* `clone`      Clone a repository into a new directory
* `commit`     Record changes to the repository
  - `-m "message"` add message `message` to the commit
* `diff`      Show changes between commits, commit and working tree, etc
* `fetch`      Download objects and refs from another repository
* `grep`       Print lines matching a pattern
* `init`       Create an empty Git repository or reinitialize an existing one
* `log`        Show commit logs
* `merge`      Join two or more development histories together
* `mv`         Move or rename a file, a directory, or a symlink
* `pull`       Fetch from and integrate with another repository or a local branch
* `push`       Update remote refs along with associated objects
* `rebase`     Forward-port local commits to the updated upstream head
* `reset`      Reset current HEAD to the specified state
* `rm`         Remove files from the working tree and from the index
* `show`       Show various types of objects
* `status`     Show the working tree status
* `tag`        Create, list, delete or verify a tag object signed with GPG

More documentation can be found on `http://git-scm.com/doc`

## Github Syntax
Github is a web-based hosting service for software development projects that
use the Git revision control system.

### Start a repo
Start a repo by going to your profile page and click on the `+` sign 
(upper righthand corner of the page) and choose _Create a new repo_.
Or go to `https://github.com/new` (you need to be logged in for this)

### Create a local copy
Open Git Bash or terminal.

* Create a directory to store the repo `mkdir <path for repo directory>`
* Navigate to the new directory `cd <path for repo directory>`
* Initialise a local git repo `git init`
* Point to the remote repo `git remote add https://github.com/yourUserNameHere/repoNameHere.git`

### Fork another user's repo
Go to the repo you want to copy and hit the _Fork_ button. 
Clone (make a local copy of a fork) the repo by going to the local folder you want to save it and
do `git clone https://github.com/yourUserNameHere/repoNameHere.git`

### Add local changes to the remote branch

* Commit your local changes (add a helpfull message)
* Pull any changes made to the remote branch (compared to when you last pulled it)
* Merge the remote to the local version (there might be conflicts)
* Push your local changes (which you have committed)

More information can be found on `https://help.github.com/`

## Markdown Syntax
This is a summary of basic markdown syntax

* `#` Heading
* `##` Secondary heading
* `###` Tertiary heading
* `*` Unordered list item (can also use `-` and others(?))
* `**text**` Bold text
* `_text_` italic text

Help on markdown can be found at

* Online introduction:  `http://daringfireball.net/projects/markdown`
* Rstudio, quick guide: Click the MD button
* R markdown: `http://www.rstudio.com/ide/docs/authoring/using_markdown`
(not needed until the _Reproducible Research_ course

## Installing R packages
Commands:

* `available.packages()` obtain available packages from CRAN 
(save to variable with `<-`, show first n  packages with `head(rownames(<var>,n)`
* `install.packages("<packagename>")` install single package from CRAN
_ Can also be done in RStudio from `Tools > Install Packages`_
* `install.packages(c("<packagename>","<packagename>"))` install multiple packages from CRAN
* `biocLite()` install basic set of Rpackages from Bioconductor 
_first add `source("http://bioconductor.org/biocLite.R")`_
* `biocLite(c("<packagename>","<packagename>"))` install the given packages from bioconductor
* `library(<packagename>)` load given package into R **!Don't use ""!* **Load depndencies first**
* `search()` show functions of loaded package
