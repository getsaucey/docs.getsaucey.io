This is Adcades' *temporarily* hosted QA Documentation site. Get started in 2 parts.

## Git
Open Terminal, and run:

	cd ~/Desktop && git clone git@github.com:sajjadhossain/AdcadeQADox.git

# `AUTHOR` get Mou 
Download [Mou](http://25.io/mou/). 

Navigate to `AdcadeQADox` folder in your Desktop. 

Then, open the `docs` folder. 

Right click on any .md file, i.e. `Click_Through_Verification.md` from `testing` folder & open with Mou.

Additionally, you can open Terminal and set Mou as an alias:

	alias mou="open /Applications/Mou.app"

Please see: [Mou syntax](http://25.io/mou/), it comes with the install as well `COMMAND + R` when your in the app.

# `ADMINISTRATOR` get MkDocs 
Admins can also author via below.

## Installation for Admins
In order to install MkDocs you'll need Python installed on your system, as well as the Python package manager, pip. You can check if you have these already installed like so:

	$ python --version
	Python 2.7.2
	$ pip --version
	pip 1.5.2

Install the mkdocs package using pip:

	$ pip install mkdocs
	
You should now have the mkdocs command installed on your system. Run `mkdocs help` to check that everything worked okay.

	$ mkdocs help
	mkdocs [help|new|build|serve|gh-deploy] {options}


## Getting Started
Getting started is super easy.

	$ mkdocs new my-project
	$ cd my-project

There's a single configuration file named `mkdocs.yml`, and a folder named docs that will contain our documentation source files. Right now the docs folder just contains a single documentation page, named `index.md`.

MkDocs comes with a built-in webserver that lets you preview your documentation as you work on it. We start the webserver by making sure we're in the same directory as the `mkdocs.yml` config file, and then running the mkdocs serve command:

	$ mkdocs serve
	Running at: http://127.0.0.1:8000/

Open up http://127.0.0.1:8000/ in your browser, and you'll see the index page being displayed:


## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
