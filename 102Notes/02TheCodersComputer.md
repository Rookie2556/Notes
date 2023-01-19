## Choosing a text editor


![Text editor](https://kinsta.com/wp-content/uploads/2019/03/notepad-plus-plus-text-editor-1-1.png)

A text editor is by google definition:

  > text editor -
  > Learn to pronounce - 
  > nounCOMPUTING -
  > a system or program that allows a user to edit text.

To us, it is the software with the capability to edit code, and usually has some sort of additional features over say... *notepad*. A bit like how artists would prefer to use Adobe illustrator, Krita etc over MS PAINT included with windows for it's features, *technically* one could become an artist in paint but it'd be **much** easier in krita as errr... graphics tablets have errrr... better compatibility *I'm guessing, I'm a computery guy not an artist*

![Krita vs MS paint](https://preview.redd.it/hs5ra12f3y881.png?width=640&crop=smart&auto=webp&s=c3500929b36b700e85ebf063d38a48a18e4c8aa3) 

![Krita](https://krita.org/wp-content/uploads/2019/08/krita-ui-40.png)

Text editors not made for coding, will oftentimes be an annoyance to format and indent code for. e.g. slightly off so you gotta backspace and space to fix it... saving extensions under "all file types" .html *ugh*. This "code" specific text editors are usually called "IDE"s which means integrated development environment.

- People, professionals even, have a preference in their text editor despite of its' importance par a few select features and can be based on visuals or unimportant features, however some useful features are:
- - Code completion - where the program guesses the rest of whatever you're typing
- - syntax highlighting - changing colours of certain keywords for easier readability
- - A nice variety of themes to choose from to "reduce eyesoreness" but eh nice colours are cool
- - Extensions selection and support, this is fairly important... should've been number 1 to be frank.

Extensions are especially useful for saving time as they usually have some modules that would otherwise take you an eternity to 'work around', e.g. Numpy in python saves you having to code your own machine learning from scratch!

Some good text editors are:

* Notepad++, free to use
![Notepad++](https://i.pcmag.com/imagery/articles/01rBnPopClrTbcmGbFMDwIE-1..v1597666892.jpg)

* VS code, free to use
![VS CODE](https://code.visualstudio.com/opengraphimg/opengraph-home.png)

* Atom, free to use
![Atom IDE](https://lunaticthinker.me/wp-content/uploads/2016/05/atom.jpg)

* Brackets, free to use
![Brackets IDE](https://www.omgubuntu.co.uk/wp-content/uploads/2017/07/brackets-for-linux.jpg)

* Sublime Text, **NOT FREE, I wouldn't pay for an IDE personally** 
![Sublime IDE](https://cdn.britannica.com/96/198296-050-65D1A810/Clowns-tour-Ringling-Bros-Barnum-Atlanta-2017.jpg)

## Terminal work

**Command line interfaces (CLI)** are usually somewhat similar across all OS with their *little* differences and usually work as such the user types in something (a command) to navigate menus/interfaces. This can give the user faster access if they know their way around, uses less resources (which is sometimes essential), doesn't always require an operating system.

However, the CLI requires expertise to use properly, they're more case sensitive than GUIs (graphical user interfaces), mistakes can do more damage and GUIs have the option to have multiple CLIs running at one time.

All Operating systems have a terminal, within which is a shell (the graphics of the terminal and how it behaves is decided by the operating system.)

BASH - Bourne again shell. - *useless information to be honest* 😘

**Basic Navigation** in WLS Ubuntu 2.04, pwd means print working directory - e.g. where you are right now; dir, meaning directory tells you what is around you. e.g. pwd would print home/Footymad, dir would expose that Footymad has dir Ronaldo.py Mbappe.md DonaldTrump.md files within that directory. cd (change directory) would change your directory to whatever is after the cd. e.g. pwd=Footymad, dir shows Ronaldo Mbappe and donaldtrump, to cd Ronaldo would make your new pwd Ronaldo.

There are two types of paths - relative and absolute. Relative is from your current pwd, absolute meaning from anywhere. Files are kept in a hierarchical style, topmost being the root and absolutes are relative to the root.

e.g. C://Users/Ronaldo/Suiiii would be applicable from anywhere, however a pwd= Ronaldo, cd Suiii would only work within Ronaldo. 

ls (lower-case Ls, meaning list, essentially same as dir), ls -a shows hidden files as well.

**About files** extensions tell the system what that file is for, e.g. .exe means executable to windows, .txt = text file, .png .jpeg *.yiff* (gif), Linux has no extensions so the os doesn't use .exe .txt .yiff!

Linux hides files by adding a . at the start, if a file is named with . at the start, it is hidden, if a hidden file is renamed to remove the . it becomes unhidden.

Text editors are important to us as without, we'd struggle to keep up effiency and comfort in our respective IDE would lower stress when errors inevitably come flying all over the place.

Todays lesson did help me out with my confidence around CLIs, I generally avoided them but today I actually preferred to use it. (*except when I accidentally deleted my entire respo but anyhow*)

In Addition to the note taking aspect, the lab taught me how to use these commands:

- git add . (Snapshots changes), the . means all
- git pull (opens file in text editor)
- git commit -m "" (Applies changes and comments the change in github)
- git clone [link] (applies the remote into local)
- mkdir (Make directory, if file mkdir'd doesn't exist, a new directory is made)
- rm (remove), rmdir removes directories, however those directories have to be empty.
- -f (force) 
- mv (renames)
- staging
- touch (creates files, however need to include file extensions e.g. .md)
- code [file] (opens in VS code)

> We've not touched most of this yet
![Cheat Sheet for WLS](https://i.redd.it/rl0fe7r6zku11.jpg)

Git is the local copy of the github, GitHub is the remote copy of the git. *depending how you see it*, they require each other to properly function.

## Things I want to know more about

- I had to type out "file1.md file2.md..." to 8 and to 15 multiple times, is there a faster way to type this out e.g. file{1-8}.md? (in the lab)
- what is worth paying £70 for an ide??!

* [Home](/102Notes/01MarkDown.md)
* [Prev (01, Learning Markdown)](./01MarkDown.md)
* [Next (03, Revisions and the Cloud)](./03RevisionsAndTheCloud.md)


