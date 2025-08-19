# Gitmagic v1.5

[![Gem Version](https://badge.fury.io/rb/gitmagical.svg)](https://badge.fury.io/rb/gitmagical)
[![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=flat&logo=ruby&logoColor=white)](https://www.ruby-lang.org/)
[![GitHub stars](https://img.shields.io/github/stars/isene/gitmagic.svg)](https://github.com/isene/gitmagic/stargazers)
[![Stay Amazing](https://img.shields.io/badge/Stay-Amazing-blue.svg)](https://isene.org)

<img src="img/gitmagic_logo.svg" align="left" width="150" height="150"> Git Made Magical - A simple and flexible gem for automating common git tasks.
<br clear="left"/>

## Usage

### Name
"gitmagic" is a swiss army knife of git tools

### Synopsis
gitmagic [-idDpusvh] [long-options]

### Description
* Initiate projects from your local folders
* Create new online presentations using Jekyll w/Gitpages
* Update projects easily
* Flexible configuration system with support for config files
* GitHub Personal Access Token support for improved security

### What's New in v1.5
* Added configuration file support (`.gitmagic.yml`)
* Added GitHub Personal Access Token authentication
* Fixed git clone command bug
* Improved code organization while maintaining backward compatibility

### Configuration

Gitmagic now supports configuration files. Create a `.gitmagic.yml` file in one of these locations:
* `~/.gitmagic.yml` (recommended)
* `~/.config/gitmagic/config.yml`
* `./.gitmagic.yml` (current directory)

See `.gitmagic.yml.example` for a sample configuration.

You can also set a GitHub token via the `GITHUB_TOKEN` environment variable.

### Options

#### -c, --clone  
Simply clones a repo, just like 'git clone'..

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

### Installation

```bash
gem install gitmagical
```

### License
Copyright 2018-2025, Geir Isene (https://isene.org) This program is released under the WTFPL license (Full license text here: http://www.wtfpl.net/about/)
