# visualizing GHG  Emissions

This repo is the start of a summer project focused on visualizing GHG emissions data. We will visualize the data primarily using the [Python](https://www.python.org/) library [Matplotlib](https://matplotlib.org/)

## Getting started

### The terminal
This is how you can send text-based commands directly to your operating system. When using the terminal there is really no need to use the trackpad, everything can be done with the keyboard. For our purposes there are only a few basic commands you need to know:
- `ls`: which lists files and directories
- `pwd`: prints the working directory
- `cd`: this stands for change directory
- `which`: displays the path a program, if it is installed

That is really all we need to know.

To open the terminal on your Mac you press Command + spacebar to open Spotlight and then type `terminal.app` and open the terminal. If you are unfamiliar with the terminal, I would suggest watching this 17 minute YouTube video [An absolute BEGINNER guide to Mac OS Terminal](https://www.youtube.com/watch?v=aKRYQsKR46I).

Don't worry, we won't be using the terminal *that* much.

### Installing Python
First make sure you have Python installed on your machine. You can check this by typing the following command into the terminal:

```sh
which python3
```

You should be prompted with the path to the Python binary. If you receive a message saying "python not found", then try `which python` instead of `which python3`. If you *still* receive a message saying "python not found" then you download the latest version of python [here](https://www.python.org/downloads/). 

### Git
You are probably reading this on GitHub. GitHub is a code repository that uses `git` to track changes. Make sure you have a GitHub account and that you have `git` installed on your computer. Check the latter with:

```sh
which git
```

If it is not installed then visit the [git webpage](https://git-scm.com/) and install it.

`git` is a very powerful program. I do not expect you to know everything command it has to offer, but you should know the basics. I would suggest watching this 10 minute video on `git` that shows you the basics. [A Brief introduction to git for beginners | GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs).


### Clone the repository
First, change into the directory you want to "clone" the repo to. This is likely something like `/Documents`. Then run the following command to clone the repo:

```sh
git clone git@github.com:lgloege/visualizing-ghg-emissions.git
```

Now you change into that directory

```sh
cd visualizing-ghg-emissions
```

### UV package manager
[uv](https://docs.astral.sh/uv/) is the best package manager for python projects, don't let anybody tell you otherwise. My favorite way to install `uv` (and to install most packages) is with [homebrew](https://brew.sh/). Homebrew can be installed by running the following command in your terminal:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once installed, you can install `uv` with

```sh
brew install uv
```

That's it, now `uv` is installed on your system. You can check this by running `which uv`. 

There are a few other ways to install `uv`, see the [installation guide](https://docs.astral.sh/uv/getting-started/installation/), but I strongly suggest using homebrew. 


### Install dependencies
This repo contains a `pyproject.toml` file that lists the necessary dependencies. To create an environment that is in sync with the one defined in `pyproject.toml`, simply run the following command:

```sh
uv sync
```

This will download the necessary dependencies and create an isolated environment for you.

### Running code
in the `notebooks/` directory I have included an example jupyter notebook. My favorite place to run code is with [Visual Studio Code](https://code.visualstudio.com/). If you do not have VScode insatlled you can either install it from the webpage or you can use Homebrew. The homebrew command is:

```sh
brew install --cask visual-studio-code
```

once installed, open the directory that contains this file with VS code. If you are in the terminal in this directory, you can run the following:

```sh
code .
```

This opens the current directory (that's what the `.` means) with VS code. 

Now from within VS code you can navigate to the `notebooks/` directory and double click on `visualize.ipynb`. This should open the code in a jupyter notebook. [Jupyter](https://jupyter.org/) is program to run code and is excellent if you are making plots. It is one way to write python code, but it is not the *only* way. 

### Matplotlib
We are going to be using Matplotlib to create plots. Matplotlib is massive, and can be a little daunting. It is easy to make a simple plot, but modifying plots can get tricky. Anything is possible with Matplotlib, but it may not always be the most intuitive. I would suggest going through the [user guide](https://matplotlib.org/3.5.3/users/index.html) and [tutorials](https://matplotlib.org/3.5.3/tutorials/index.html).