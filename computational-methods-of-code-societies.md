# Computational Methods of Code Societies
Day 2 ~ Code Societies ~ Winter 2019

Taught by Melanie Hoff & Nabil Hassein

✿ this guide was compiled by emma @doodybrains rae norton

_🍃The computer, the programmer, the relationship they have with each other, and the environments they create🍃_

A one-session class covering the primary computational methods of Code Societies Classes: Winter 2019. Together we will defamiliarize and refamiliarize ourselves with the Command Line Interface, Git/Github, running Python 3 in the terminal, & running Python 3 with Anaconda Jupyter Notebook. We will navigate folder structure narratives with the command line, time travel with Git, code socially with Github, and process language with Python.

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

1. Run `cd ..` as many times as you need until your bash prompt tells you that you are inside of the `computational-methods-code-societies` folder
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

## 🌿What is git??
> A version control and time travel software! Suspend your belief for just a moment!

To begin `cd ..` and `cd ..` again until you are inside `computational-methods-code-societies`

✨Enter the command: `git init`
Now follow these steps:
1. `git add .`     
2. `cd time-travel/`
3. `ls`
4. You should now see a folder called `sensations.txt`
5. `atom .`
6. Edit the `sensations.txt` file in Atom
> For the next 60s ⏲, inside the `sensations.txt` file write down the small sensations and sounds you’re experiencing right now in this moment. Volume of words > coherence
7. Save the file and go back to terminal.
8. `git commit -am “my first sensations”`

> Repeat steps 6 - 7 two more times; 

9. Make sure you `git commit -m “my second sensations”` + `git commit -m “my third sensations”`
10. `git log`
11. Copy one of the hashes from one of your commits. The hash looks something like this `6c750cb264c6d5ad0fac18863cafd0df35315fce`
12. Press `q` to exit log
13. `git show <place your hash here>` this allows you to review the detailed history of a given change

> Now we’re going to time travel!!

14. `git checkout <place the hash of your first commit here>`

> This is like traveling through time to past versions of yourself and the record of the sensations you were feeling at multiple distinct moments in the past 🔮

15. Advanced, optional: rewriting history with `git rebase`

## 🌿What is GitHub?
Git is an open source software that GitHub capitalizes on. Git allows for collaboration. GitHub will allow you to save, and edit and update your code. For this guide we will be pushing our Folder Strucuture Narrative up to a new GitHub repository

Make sure to run `git checkout master` to go back to your latest code (all three sensations).

1. Login to GitHub or create account.
2. Go to repositories page and click new, 
3. Name it `computational-methods-code-societies`
4. Click the Create Repository button
5. Type `git remote rm origin` (this ensures that you will be able to add your own github repository as the origin)
6. Follow the instructions at your GitHub repository for “push to an existing repository”
7. Copy each of the following commands one at a time, paste it into the terminal and press enter
8. git remote add origin <YOUR URL HERE>
9. Before running the following command you should ensure that all of your files and folders are ready to be added to your repository. You can do this by running `git add .` Keep in mind that git only cares about files, so it will not upload folders if they don’t have files inside of them.
10. Now you can run `git commit -am “name of message”` (the message describes what you are adding)
11. Now type `git push -u origin master` (the name origin is just a naming convention and is referring to the url for your repository)
12. Prompt for username and password: Passwords are invisible in terminal
13. Optional: setting up ssh keys, if you don’t want to constantly enter your username and password

Common workflow:
`git pull`
make changes
save file changes 
run `git status` to see a list of what files changes have been made
`git commit -am “my changes message”`
`git push`

#### Partner Activity

1. Fork the `computational-methods-code-societies` repo of your partner 
2. Rename this forked repo on your github via the Settings button to include their name
3. Press the green Git Clone button and copy paste: `git clone <the url of the forked repo>` into your terminal (make sure that you are doing this inside your home directory)
4. Now you have a copy of your partner’s repo on your computer.
5. Take a look at your partner’s invented Folder Structure Narrative from earlier in class. 
6. Using terminal, build on top of what your partner was going for with their narrative.
7. `git add .`
8. `git commit -am “my addition to my partner’s narrative”`
9. `git push`

## 🌿Python
There are a lot of different ways to interact with Python. One way is using the interactive interpreter. Another way is using Jupyter Notebooks. In this guide we will mostly be working within a Jupyter Notebook.

> Don’t forget to check out Nabil’s workshop Mathematics as Religious Experience on Dec 23 

#### To ensure that Python is installed:
Type word python and press enter you should get back something like this Python 3.7.1 (default, Dec 14 2018, 13:28:58)[Clang 4.0.1 (tags/RELEASE_401/final)] :: 

#### Python terminology + conventions
In terminal you can write `print(hello world)` and the terminal will print out the line "hello world". In Python you will usually write the name of the function, open parentheses, argument, closed parentheses

> When learning to program make sure to give yourself time! Check out the book _Teach yourself programming in 10 years_

Now we will do some more things with Python:
1. Open atom
2. Create a new file
3. Paste in the following:
	`sensations = open(“sensations.txt”)`
4. Creating a variable that is going to store the information inside sensations.txt. Open is telling my computer to looks for a file called sensations.txt within the directory that you are currently in. Don’t forget to use quotations for your file name!
5. Now add print(sensations)
    This will print out whatever is inside of the variable sensations. Terminal will return:
	`<_io.TextIOWrapper name='sensations.txt' mode='r' encoding='UTF-8'>`

## Loops

In the sensations.txt file add the following lines:

```sh
for line in sensations:
	print(line)
```

The sensations.txt file should now look like this:

```sh
sensations = open("sensations.txt")

for line in sensations:
	print(line)
```
Now you can save the file and go back to the Terminal.

In the terminal you can write `jupyter notebook` and press enter. This will automatically open up a new browser window.

> Programming is like magic :) 

Click on `Introduction to Python` file.

##### How can we work with these python notebooks?

Here is a list of Jupyter Notebook Keyboard Shortcuts:
- shift + enter run cell, select below.
- ctrl + enter run cell.
- option + enter run cell, insert below.
- A insert cell above.
- B insert cell below.
- C copy cell.
- V paste cell.
- D , D delete selected cell.

- Use down arrow key to navigate to next section or block of code

- When clock of code is highlighted in blue you can press command enter (or control enter) to run it (you can press the button also!)

- Debugging 

![First Computer Bug - Image ©Courtesy of the Naval Surface Warfare Center, Dahlgren, VA., 1988. NHHC Collection](https://media.wired.com/photos/5b173a76747c6a7f99f901a4/master/w_740,c_limit/moth.jpg)

> think like a scientist and come up with a hypothesis for what you think is going on then do a series of test to try and prove yourself wrong

- Once we have gotten to the end of the file remember that we need to open the file again before we can successfully run it!

- Make sure to read the error messages. Try your best to understand what the computer is saying.

For example:
	- `Traceback (most recent call last)` is referring to the most recent place in the code where an error was found 
	- `Io` stands for input ouput
	
##### Perhaps the #1 programming skill is “googling the error message”

More resources:
- https://drive.google.com/file/d/1gxjTV0SjIgedS7mGaLGwwf6_-7w380lL/view
- https://devhints.io/
