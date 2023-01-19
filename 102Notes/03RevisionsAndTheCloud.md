# Git Intro

Git is defined as >a distributed version control system: tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows.
developers of git back in 2002, created "BitKeeper" which was similar to the git we know and love 💙 which underwent drama 
and its' developers then developed Git in 2005.


Git is **GREAT** for version control, in CLI it can save us time and time again when we decide to implement sketchy 'features'
It'd saved me twice already, when I accidentally made submodules that were identical to the repository it resided within, I tried
using CLI commands I didn't quite fully grasp, deleting all my work 😭 - but it *Saved* me 👼 👼 👼

Git is the local repository, as such it is saved on your machine. We add . commit and upload to github, if any changes are bad, 
we can simply restart and not save anything to github.

Github is essentially the central node in version control, and Git is each persons' individual node that are able to contribute.

There are two types of Version control:

 -  -CVCS (Centralised Version control) - e.g. Github, we rely on a server to *hold* all our versions collectively.
 -  -DVCS (Distributed Version Control) - e.g. Git, we rely on a machine to hold the most recent verion via snapshot per usual.

Obviously both can fail and a hybrid of both is possible through backups on the 'other' option. It is more likely that a DVCS
is to fail rather than an industrial server like github, but github may go down for maintenance, get DDOS'd et cetera.

Git is useful for reversibility, which can avoid *cough*deletingentirerepositories*cough* and doesn't require an internet connection.

Git holds all files in one of 3 states:

 -Commited, data is stored locally
 -modified, data has been changed locally but not commited e.g. not pushed to github version.
 -staged, flagged to be commited in next snapshot
 
 ![3 states of Git files](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)
 
 ## Getting started with GIT
 
 There are 3 ways to install git:
 + Install as a package e.g. cli
 + install via an installer
 + Download and compile source code.
 
 There are multitudes of guides on how to download and use Git, some even having GUI's which I personally don't have but *anywho*
 
 ##Commands within Git
 
 **First time using git:**
 git config --global user.name "First Last"
 git config --global user.email "Email@email.com"
 
 git config --global core.editor "code --wait" - Sets VS code as your default editor when you pull or attempt to make changes.
 
 git help command - gives you help to find the apropriate commands.
 
![Git Cheat sheet](https://www.git-tower.com/blog/media/pages/posts/git-cheat-sheet/0300e8b724-1673353125/git-cheat-sheet-large01.png)
 
 The Above is fairly useful, however within minutes of using git - You get used to it!
 
 - cd means Change directory, to change directory means to change pwd to whatever. e.g. cd Ronaldo would place you in the Ronaldo file.
 
 - git init - initialises the git, e.g. makes a new git repository.
 
- $ git add *.c
- $ git add LICENSE
- $ git commit -m “any message here” 

^ above tracks the code, however I haven't done this 😲 Code is either tracked or untracked, I have tracked code before just not in this style.

- git clone brings the current version in github to your git, e.g. makes a copy for you to edit. 

Working directory -add-> Index -commit-> Head
Files reside here     staging area       points to most recent commit (*like a snek ssss*)
![Local repo structure](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)

![Life Cycle of file status](https://blog.udemy.com/wp-content/uploads/2015/08/image006.png)

Can check where we reside in the cycle by putting in > git status

git add . means to add all changes, this is the only way I've tried to track code.
you *can specify* what part you'd want to track by replacing . with filenames...

to commit a file, you type: > git commmit -m "Comment that will be seen on github"
to commit all changes > git commit -a

git push - publishes this in github.

git stashing - when a change isn't wanted to be published nor lost. > git stash

 ## Things I want to know more about

- In what instance would someone stash a change, seems like it'd get complicated fast. 
- >- $ git add *.c
- >-$ git add LICENSE
- >-$ git commit -m “any message here” 
- in what instance is the above actually used?
- Is there a way of structuring better in HTML than I've shown?


* [Home](../README.md)
* [Prev (02, The Coder's Computer](./02TheCodersComputer.md)
* [Next (04, Structure web pages with HTML)](./04StructureusingHTML.md)

