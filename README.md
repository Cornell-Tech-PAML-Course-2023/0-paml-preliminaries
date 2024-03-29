# Practical Applications in Machine Learning - Preliminaries

The goal of this activity is to help students become familiar with basic data types, data structures, functions, machine learning and numpy libraries. 

# Installation

## Downloads for course
* [Python (at least v3.5)](https://formulae.brew.sh/formula/python@3.8)
* [Visual Studio Code](https://code.visualstudio.com/)
* [pip](https://www.geeksforgeeks.org/how-to-install-pip-in-macos/)
* [Git](https://git-scm.com/downloads)
* [Jupyter Notebook](https://ipython.readthedocs.io/en/stable/install/install.html)
* [Create Google Colab Account](https://colab.research.google.com/)

## Download this repository
To install this repository and run the Jupyter notebooks on your machine, you will first need git, which you may already have. Open a terminal and type `git` to check. If you do not have git, you can download it from [git-scm.com](https://git-scm.com/).

Next, clone this repository by opening a terminal and typing the following commands (do not type the first `$` on each line, it's just a convention to show that this is a terminal prompt, not something else like Python code):

    $ cd $HOME  # or any other development directory you prefer
    $ git clone https://github.com/Cornell-Tech-PAML-Course/0-paml-preliminaries.git
    $ cd 0-paml-preliminaries

If you do not want to install git, you can instead download [master.zip](https://github.com/Cornell-Tech-PAML-Course/0-paml-preliminaries/archive/refs/heads/main.zip), unzip it, rename the resulting directory to `0-paml-preliminaries` and move it to your development directory.

## Install Anaconda
Install Python [download and install Anaconda](https://www.anaconda.com/distribution/), which is a great cross-platform Python distribution for scientific computing. It comes bundled with many scientific libraries, including NumPy, Pandas, Matplotlib, Scikit-Learn and much more, so it's quite a large installation. If you prefer a lighter weight Anaconda distribution, you can [install Miniconda](https://docs.conda.io/en/latest/miniconda.html), which contains the bare minimum to run the `conda` packaging tool. You should install the latest version of Anaconda (or Miniconda) available.

During the installation on MacOSX and Linux, you will be asked whether to initialize Anaconda by running `conda init`: you should accept, as it will update your shell script to ensure that `conda` is available whenever you open a terminal. After the installation, you must close your terminal and open a new one for the changes to take effect.

During the installation on Windows, you will be asked whether you want the installer to update the `PATH` environment variable. This is not recommended as it may interfere with other software. Instead, after the installation you should open the Start Menu and launch an Anaconda Shell whenever you want to use Anaconda.

Once Anaconda (or Miniconda) is installed, run the following command to update the `conda` packaging tool to the latest version:

    $ conda update -n base -c defaults conda

> **Note**: if you don't like Anaconda for some reason, then you can install Python 3 and use pip to install the required libraries manually (this is not recommended, unless you really know what you are doing). I recommend using Python 3.8, since some libs don't support Python 3.9 or 3.10 yet.

## Start Jupyter
The notebooks in this project will default to the environment named `python3`, so it's best to register this environment using the name `python3` (if you prefer to use another name, you will have to select it in the "Kernel > Change kernel..." menu in Jupyter every time you open a notebook):

    $ python3 -m ipykernel install --user --name=python3

And that's it! You can now start Jupyter like this:

    $ jupyter notebook

This should open up your browser, and you should see Jupyter's tree view, with the contents of the current directory. If your browser does not open automatically, visit [localhost:8888](http://localhost:8888/tree). Click on `index.ipynb` to get started.

Congrats! You are ready to learn Machine Learning, hands on!

When you're done with Jupyter, you can close it by typing Ctrl-C in the Terminal window where you started it. Every time you want to work on this project, you will need to open a Terminal, and run:

    $ conda env create -f environment
    $ conda activate tf2
    $ jupyter notebook

## Update This Project and its Libraries
I regularly update the notebooks to fix issues and add support for new libraries. So make sure you update this project regularly.

For this, open a terminal, and run:

    $ cd $HOME # or whatever development directory you chose earlier
    $ cd 0-paml-preliminaries # go to this project's directory
    $ git pull

If you get an error, it's probably because you modified a notebook. In this case, before running `git pull` you will first need to commit your changes. I recommend doing this in your own branch, or else you may get conflicts:

    $ git checkout -b my_branch # you can use another branch name if you want
    $ git add -u
    $ git commit -m "describe your changes here"
    $ git checkout master
    $ git pull

Next, let's update the libraries. First, let's update `conda` itself:

    $ conda update -c defaults -n base conda

And recreate the environment:

    $ conda env create -f environment.yml

Lastly, we start Jupyter:

    $ jupyter notebook

Open the files listed below and follow along in lecture to complete them:

* 1-hello-world.ipynb: explore data types, data structures, simple operations (addition, multiplication, etc), and functions
* 2-ML-libraries.ipynb: explore ML libraries e.g., pandas to store data, create visualizations
* 3-numpy-tutorial.ipynb: Use numpy to store arrays, matrices, lists, and other data types

# Further Issues and questions ❓

If you have issues or questions, don't hesitate to contact the teaching team:

* Angelique Taylor (amt298@cornell.edu) - Instructor
* Tauhid Tanjim (tt485@cornell.edu) - Teaching Assistant
* Jinzhao Kang (jk2575@cornell.edu) - Grader
* Kathryn Gdula (kg435@cornell.edu) - Grader