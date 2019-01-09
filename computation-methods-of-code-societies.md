# Computational Methods of Code Societies
Day 2 ~ Code Societies ~ Winter 2019

_🍃The computer, the programmer, the relationship they have with each other, and the environments they create🍃_

## 🌿Before we begin...
- You should have the following programs installed on your system:
    - Atom
    - Git
    - Anaconda
    - You should also have a GitHub account
- Original syllabus lives here: https://docs.google.com/document/d/1nTAGOnsBCW5pTe0KfKtdEfqeSwC8YuFhBSad0Xu_Zdw/edit#heading=h.j1gmhmtgvufk
- Download the folder at this link: https://drive.google.com/file/d/1DtBmjeguFjsyHmj8oqADk8NEv14g1bCh/view
- Unzip the folder and move it into to your “home” or "root" folder (the one with the little house icon on a Mac).

## 🌿We can think of the “environment” as way that a programmer builds their personal workflow in the domain of their computer…
> Coding isn’t something that just happens in your text editor or terminal. Coding can be a wholistic computer practice, a new relationship you have with your computer & your computer habits. from the way you name your files or organize your folders, to completely changing how you perform routine tasks on your computer such as moving a file.

To ensure that you can easily access Atom (the text editor we will be using throughout this guide) follow these steps:

1. Open Atom
2. Click the Atom menu in the top left corner and choose “install shell commands”. This will ensure that you can access Atom from the Terminal also known as the *command line*.

## 🌿What is the command line?
Think about all of the applications you open on a day to day basis on your computer. One of the many mechanisms we use to do these things is dragging and clicking different icons and folders using a mouse or trackpad. 

Let’s take a small tour of our computers by following these steps:
1. Open up a new Finder window. 
2. Navigate to your home folder. It is helpful to use the “folder view”, you can do this by clicking the little icon with the three rectangles at the top of the Finder window.
3. Click on the code-societies folder
4. Notice that there are two folders inside of that folder
5. Now click on the computational-methods-code-societies folder
6. Notice that there is a folder called house
7. If you click on house you will notice a few more folders denoting the rooms in the house
8. Keep going!

> This folder structure follows the structure of a house which is a spatial metaphor for how we navigate folders on our computer. For example, when you’re in a house and standing in the kitchen and you wanted to go to bed you would need to navigate from the kitchen into your bedroom before you actually tried to lay down.

Another way to do this kind of navigation is by using the command line, a text-based mechanism for doing the same kind of navigation between folders and files. 

The command line can be seen a more intimate way to interact with your computer, it’s kind of like having a conversation, you can ask your computer to do something and it might respond to you with a confirmation of what you typed or some kind of prompt or a scrolling list of crazy words letting you know that it is in the process of installing some stuff or nothing at all! 

> sometimes you will ask your computer to install something and it will not give you any kind of response but the thing you wanted to install was actually successful. the reason the computer will not return any kind of response takes us way back into the history of computing when the computer would respond to a programmer by printing out its response on a piece of paper. In order to save paper computers were programmed to just do nothing if the command was successful.

## 🌿Lets embark on a Folder Structure Narrative !

> Moving forward you can think of the Terminal (command line) as the “secret trap door/master key/teleportation portal” to your computer.

The programming language of the terminal is called Bash. This is the language that allows us to write commands that the Terminal can understand so that we can do things like navigate the file system (as we did above) on our computers. Bash files, also known as scripts because they often execute pieces of code, look something like this `name-of-bash-script.sh`

Follow these steps to begin:

1. Press command and spacebar
2. Type in “Terminal”
3. Press Enter
4. When you open the Terminal you’ll see something called a bash prompt: You’ll see your user name and a `~` The `~` represents your home directory.
5. You can verify that you’re in the home directory by typing `ls` and pressing enter. You should see a list of all of the folders and files directly inside of your home directory.
6. You change directories from your home directory by typing `cd` and pressing enter.
7. If you type in `cd code-societies` your bash prompt will now look something like this `your username:code-societies$`
8. Remember you can verify that you’re in the a particular directory by looking at your bash prompt as well as by running the `ls` command. With the `ls` command you should see all of the folders and files inside the directory you are currently in.
9. From the `code-socities` folder you can cd into `computational-methods-code-societies`
10. Finally you can cd in the house folder.
11. Welcome to the house tour! Lets `cd` into the `kitchen`! 
12. Run `ls`. Do you see the file `pots-and-pans.txt` ?
13. Try running this command `cat pots-and-pans.txt`
14. This `cat` command will display all of contents of that file right inside your terminal ! How beautiful !
15. Now you lets `cd` into the `garden`
16. Run ls again and notice a file called `grow.sh`. We know this is a bash script because of the `.sh`. This means that we can execute this script (or program) inside of terminal. 
17. To see the bash script in action type `bash grow.sh` and press enter. A bunch of beautiful flowers should appear! 
18. Notice if you run `cat grow.sh` you will see the contents of the script that produced the bunch of beautiful flowers!

The commands we’ve learned so far are:
`cd`
`ls`
`cat`
`bash`

Some more helpful commands:
`pwd`
`open .`
    opens the folder you are currently inside of
`cd ..`
    changes directories in reverse
tab key to autocomplete
up and down arrow keys
`touch`
    creates a new file
`atom .`
    opens the folder you are currently inside of with Atom
`mkdir`
    makes a new directory
`touch myfile.txt`
    creates a new file called myfile.txt
`rm foldername`
    removes a folder called foldername
`rm filename.txt`
    removes a file called filename.txt
`say`
    asks your terminal to say whatever you have types

> If you try to run cat on a jpg file the terminal will print out all of the “text” for the file. 

## 🌿Now you can create your _own_ Folder Structure Narrative
> Example of artist, Ryan Kuo who used navigating a generic looking Mac Application to talk about navigating family dynamics in his piece, [Family Maker](https://www.dropbox.com/s/ra6gl7hakv4n3qg/Screenshot%202019-01-08%2013.34.51.png?dl=0)

1. Run cd .. as many times as you need until your bash prompt tells you that you are inside of the `computational-methods-code-societies` folder
2. We will use the `mkdir` command to create some new folders. mkdir stands for make directory. For example, you can run `mkdir my-new-folder` and that folder will be created inside of your `computational-methods-code-societies directory`. 
3. Use the touch command to create new files within the folders. It is helpful to make sure that the names of your folders and files do not have spaces or capital letters
4. Use `cd name-of-folder` and `cd ..` to move in and out of folders
5. Use `rm -rf name-of-folder-or-file` (remove recursive force) to delete items but be careful you can’t undo this!
6. If you see a bash command and you want to know exactly what it does you can use the man command, for example `man ls` will show you what ls stands for. You can press `q` to exit the explanation. 
7. If you want to see hidden files (files that start with a dot) within a directory you can run `ls -AF`
8. You can run the `clear` command to refresh your terminal window.

### 🌵Some more Folder Structure Narrative examples
| Subject | Link |
| ------ | ------ |
| City of my dreams | https://github.com/doodybrains/computational-methods-code-societies-iris/tree/master/cities-in-my-dreams |
| A physical desktop | https://github.com/mimidoan/methods |
| A bodega | https://github.com/a-sparse-city/computational-methods-code-societies/tree/master/bodega |
| Universe of Tushar | https://github.com/Saltzshaker/universe-of-tushar-computational-methods-code-societies-1 |
| The roots: a plant | https://github.com/jarretbryan/acgillette-computational-methods-code-society |
| Champagne glasses | https://github.com/acgillette/computational-methods-code-societies-jarret/tree/master/champagne_glass |
| Clouds | https://github.com/mattohagan/yesmoon-computational-methods-code-societies
| Space |https://github.com/yesmoon/mattohagan-computational-methods-code-societies
| Guilty pleasures |https://github.com/nadjao/computational-methods-code-societies-sonny
| Semantic world of familiar things | https://github.com/nicolch/computational-methods-code-societies
| Levels of hunger | https://github.com/sonnynomnom/computational-methods-code-society-nadjao
| Crowded train | https://github.com/iris-qu/computational-methods-code-societies-emma-rae
| Basic | https://github.com/vcampbell89/computational-methods-code-societies
| House | https://github.com/asd0999/emily-s-computational-methods-code-societies-1
| Stages of Life |  https://github.com/csanchez73/ingrid-computational-methods-code-societies
| College Home | https://github.com/ilange/Carlos-computational-methods-code-societies
| Order of activities after waking up |
| People met today |
