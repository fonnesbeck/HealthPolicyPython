**Table of Contents**

- [Python Programming for Health Policy](#python-programming-for-health-policy)
- [Syllabus](#syllabus)
- [Installing Python](#installing-python)
	- [Download](#download)
	- [Install](#install)
	- [Check your installation](#check-your-installation)
	- [Create a virtual environment](#create-a-virtual-environment)

# Python Programming for Health Policy
### Python programming workshop for Vanderbilt's Department of Health Policy

**December 16, 2015**

The goal of this workshop is to very briefly introduce health policy researchers to the Python programming language, and illustrate how it can be used for data cleaning, exploration and analysis. Given the constraints of a two-hour time slot, we will try to use the first part of the workshop to provide an overview of programming in Python, including data structures, control flow and function-writing, while the second part will be an example-driven tour of Python's data analysis functionality, with links to additional external information for those interested in learning more about any given aspect of the material.

For participants who would like to follow along with the workshop as a hands-on tutorial, I have provided instructions below on how to install Python on your computer. 

## Syllabus

Introduction to Python

Data Analysis Using Python

## Installing Python

If you wish to follow along with the tutorial materials on your own machine, you will need to download and install Python, and set it up with the appropriate data analysis packages. I recommend using Anaconda Python distribution because it is easy to get up and running, and comes bundled with most of the packages you will need.

To download the course materials, you can either clone this repository using `git`, or if you are not familiar with `git`, just download a zip file of the repository using the button near the upper right hand side of this page.

### Download

Go to the [Anaconda download page](https://www.continuum.io/downloads) and download the Python 3.5 installer for your operating system.

### Install

Double click the Anaconda installer. A user interface will pop up to guide you through the installation.

For details on installing Anaconda Python, see [the official guide](http://docs.continuum.io/anaconda/install.html).

### Check your installation

If you installed Anaconda successfully, then in a new terminal window you should have access to the `conda` command. Try typing it in and running it; If you get a `command not found` error, then the Anaconda directory is probably not in your `PATH`. Please contact the tutorial instructor for assistance.

### Create a virtual environment

A really nice feature of using Anaconda for data analysis is that you can create isolated *environments* for particular projects you are working on. In the environment, you control exactly which packages (and which versions) are available, making it easier to replicate or share development environments between machines or people.

I have created a file called `environment.yml` that contains instructions for creating an environment for this tutorial. The contents of that file are simply as follows:

```yml
name: healthpolicy
dependencies:
    - python=3.5
    - numpy
    - pandas
    - jupyter
    - matplotlib
```

It is just a list of the packages we need, along with a name for the environment.

Move into the directory that contains the tutorial materials and run this `conda` command to create this virtual environment:

`conda env create`

Now you can enter your environment with this command:

`source activate healthpolicy`

Your command line prompt should look something like this:

```bash
(healthpolicy)user_name@machine_name:~$
```

To leave the environment, use this command:

`source deactivate`

### Running Jupyter Notebooks

The course materials are provided in the form of [Jupyter notebooks](http://jupyter.org). This is an interactive, web-based interface to Python that allows code, text and other supporting media to be integrated in a robust analytics environment. Having set up and activated your environment above, you can run Jupyter from the command line as follows:

`jupyter notebook`

This will automatically open your web browser to a list of available files in the project directory, including the notebooks containing the workshop materials, in files with a `.ipynb` extension. Clicking on any of these files will open the notebook and allow you to work with them interactively.