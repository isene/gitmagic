# Gitmagic

## Usage

### Name
"gitmagic" is a swiss army knife of git tools

### Synopsis
gitmagic [-idDpusvh] [long-options]

### Description
* Initiate projects from your local folders
* Create new online presentations using Jekyll w/Gitpages
* Update projects easily

### Options

#### -i, --init  
Initialize a new github project.
Requires a name for the repo as argument
You also need to supply --desc (-d) and a description of the repo
You may supply a dir path "--dir" (-D), or else the current dir is used
EXAMPLE: gimagic -i "My new repo!" -d "Really cool stuff" -D ~/projects/124

#### -d, --desc
Add description to a new repo
Used in combination with --init or --slides

#### -D, --dir
Specify the directory for a new initiated repo
Used in combination with --init or --update
If no directory is specified, the program will use the current directory

#### -p, --priv
Make the Github repo private

#### -u, --update
Update a github project
Takes the commit message as argument
You may supply a dir path "--dir" (-D), or else the current dir is used
EXAMPLE: gimagic -u "Bug fix" -D ~/projects/159

#### -s, --slides
Create a presentation project with slides written in simple Markdown text.
See Fredrik Eilertsen's neat work that makes it possible to create 
presentations using Jekyll (https://github.com/fredeil/gh-presentation)
This option will use '$pres_templ' to find the cloned "gh-presentation"
It will create the presentation under your '$repodir'
You must supply a name for your repo/presentation as the argument
EXAMPLE: gimagic -s "Presentation23"

#### -v, --version
Show the version of this program

#### -h, --help
Show this help text

### License
Copyright 2018, Geir Isene (https://isene.org) This program is released under the WTFPL license (Full license text here: http://www.wtfpl.net/about/)
