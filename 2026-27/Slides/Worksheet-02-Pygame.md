<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>

# Pygame

## Install VSC, Python and Pygame

### Visual Studio Code & Python

1. Open a web browser
2. Enter `app` in the search bar
3. Autocomplete should bring up `Apps Aywhere` - select it and load the page
4. In the search box on the page enter `visual studio code` and search for VSC
5. Select `Visual Studio Code` and install it.
6. It will probably say `Python` needs to be installed, do that then circle back to 7. All being well you should now be able to run VSC from the start menu. It should launch automatically.
8. Install required extensions - `Python Extension Pack`, `Git Extension Pack`
9. Ensure you've set up your computer for git

```console
git config --global user.name "Andy Guest"
git config --global user.email "a.guest@yorksj.ac.uk"
```

### Install Pygame-ce

In VSC open a terminal from the menu bar. 

Install pygame-ce in the terminal with:

`python -m pip install pygame-ce`

Upgrade if needed:

`python -m pip install --upgrade pygame-ce`

### Verify Installation

In the terminal type

```console
python

import pygame
print(pygame.version.ver)
```

If no errors occur installation was successful.

Type `exit` to exit python.

---

## The quick demo

### Download the repository

1. `File` > `Close Folder` if you have a folder open in VSC
2. On the welcome page click `Clone Git Repository`
3. In the box that pops up paste `https://github.com/andyguestysj/BasicSetup.git` and press enter
4. Browse to the folder you want to put the _downloaded project folder in_. Not the folder you want the code in but the folder you want the folder in. And press enter
5. Wait a bit and then select `Open` or `Open in New Window` as you prefer.

### Disconnect from my repository

1. After downloading the repository
2. Click the `Source Control` icon on the LHS toolbar. It looks like three circles connected by two lines.
3. Mouse over `CHANGES` then click on the three dots to the right of `CHANGES`.
4. From the pop up menu select `Remote` then `Remove Remote`
5. Click on `Origin` in the drop down list at the top of the VSC window.

You are now disconnected from my repo. To create your own ensure you have a github account and you are connected to it in VSC.

### Change to your repository

1. Ensure you have a github account set up and VSC connected to it first.
2. In the `Source Control Window` click in the `Message` box and enter a useful, informative message. Something like `Forked from https://github.com/andyguestysj/BasicSetup.git` might be good
3. Press `Publish Branch`
4. In the text box at the top of the VSC window give the repo a name you want (or leave it unchanged).
5. Click one of the two `Publish..` lines below the text box
   1. `Publish to Github private repository` will give you a repo only you can see
   2. `Publish to Github public repository` will allow anyone to see the repo if they have the URL. It won't let them change it. Generally this is the option you want. It is **definately** the option for coursework submissions.
   3. You may need to enter your github username and password.

### Running the demo

1. Click the explorer icon (looks like sheets of paper) in the icon bar
2. Select/open the file `game.py` from the explorer browser
3. Click the triangle `play` button at the top right of the code window.
4. Press `Esc` or click the close button on the game title bar to exit the game.

### The Code

1. Read through the code. 
2. Make sure you understand where the code is for the following
   1. initialisation
   2. dealing with key presses
   3. updating the game (even if there isn't any code there :-)
   4. drawing to the screen
   5. the game loop
3. Try changing aspects of the game

### Pushing to your repository

To save the game, should you wish, you can push the changes you've made to the repository you've created on your github account.

1. Click the `Source Control` icon in the tool bar
2. Enter an informative message about the update in the `Message` text box.
3. Press the blue `Commit` button
   1.  You may need to enter your github username and password.

---

## Mini Pygames

There are a number of mini pygames in this repository [https://github.com/Leonardpepa/pygame-simple-examples.git](https://github.com/Leonardpepa/pygame-simple-examples.git). They aren't polished but they will give you a feel for the basics.

The Pygame-CE documents and tutorials are here [https://pyga.me/](https://pyga.me/). If you want to dig in to how they work.

