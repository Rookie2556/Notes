## Git Intro

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

##HTML:

### Wireframing, what is it and what do I do?

Wireframing is a practice of designing an estimate for the website in mind, commonly used by UX designers.
It is a great way of getting everyone's concept of the app/software/website to be as similar as possible and avoid conflicting ideologies. **compatibility and easeability**

Wireframes can be done *anywhere* (though I'd bet digitally is the best bet on a professional standard), from pen and paper to using software. 

This was my wireframe for this project: 

![Wireframe](https://user-images.githubusercontent.com/122787483/213161145-493a5a18-8c4b-4f5a-aa5c-6a35f490076e.png)

- I put where I want the information and the images to go, typically alternating sides.
- The title was decided before the wireframe started.
- We then planned out what cakes we wanted to represent and the sizing of the imagery
- I started coding this immediately after in just HTML.

![BakingBadHTMLpic](https://user-images.githubusercontent.com/122787483/213159412-c36546d5-85a0-4742-bdb1-fcef8039ccb1.png)

*the result is not similar yet, but the HTML structure is ready for CSS to change it appropriately*

Typically wireframes can be interactive, multiple pages long to emulate what the user sees after each click etc, or basic like my example! 

There are tools out there that are massively useful, according to https://careerfoundry.com/en/blog/ux-design/how-to-create-your-first-wireframe/#what-is-a-wireframe 

- UXPin, 
- InVision
- wireframe.cc
**are good software to use for wireframing.**

3 priniples to ensure quality wireframes:

1 - Clarity, It stays true to its' purpose
2 - Confidence, the wireframe should increase every individuals confidence towards the end goal
3 - Simple, the wireframe should stick to being a wireframe and in order to do that too much detail is unecessary

### Now we know what our website looks like conceptually now what?

*Glad you asked!* 
We then structure it in HTML, HTML is hypertext markup language.
Markup is essentially just a *little* harder than markdown which we've already covered.
as such a paragraph is (opening)<p> between elements </p>(closing) and **<always have to be closed/>**

Usually, <p> <b> </b> </p> - nesting is fairly useful:

    *<p> paragraphhhhh paragraphhhhhh
    <b> **Paragraphhhhhh** </b>
    paragraphhhhhhh </p>

and the correct syntax is first opened, last closed.

if the element has no content, it is a **void** element!

    <!DOCTYPE html>
    <html lang="en-US">
     <head>
       <meta charset="utf-8" />
       <meta name="viewport" content="width=device-width" />
       <title>My test page</title>
     </head>
     <body>
       <img src="images/firefox-icon.png" alt="My test image" />
     </body>
    </html>

All html files have similar structure, <!doctype html> <html> <head> Title </head> <body> main content of page> </body> </html>

### IMAGES whoooo

Images are done using img src=path alt=if can't load, what text replaces it with < and > on both sides 😢
*github reads the img so I cannot do it correctly here*
![Imglink](https://www.simplilearn.com/ice9/free_resources_article_thumb/adding-html-images.PNG)

### most common html elements:

- <h1> **huge text </h1> <h6> <sup><sub>Add your tiny text</sub></sup> </h6> 
- <p> paragraphs </p>
- <ul> lists </ul> <ol> ordered </ol>
- <a> link </a> href would make it like the example given above.

 ## Things I want to know more about

- In what instance would someone stash a change, seems like it'd get complicated fast. 
- >- $ git add *.c
- >-$ git add LICENSE
- >-$ git commit -m “any message here” 
- in what instance is the above actually used?
- Is there a way of structuring better in HTML than I've shown?
