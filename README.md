To-Do-List
===========

To-Do List is a Web Application for creating lists.

The technology used is [Django](https://www.djangoproject.com/) (Python web framework).

The Django version used is **1.7.1**

This Web Application uses **TDD (Test Driven Development)** strategy for development.Code is written after a test.

![TDD](http://i.imgur.com/NMjYd8f.gif)

##  Creating a local development environment using virtualenv(wrapper) and pip
### Use pip to install virtualenv and virtualenvwrapper

```console
sudo pip install virtualenv
sudo pip install virtualenvwrapper
```

virtualenv is something you can use to create an isolated Python development environment. This helps isolate your dependencies, especially when used with pip. virtualenvwrapper provides some convenient short-hand shell commands to make virtualenv nicer to use. Documentation is at
[http://virtualenvwrapper.readthedocs.org/en/latest/](http://virtualenvwrapper.readthedocs.org/en/latest/)

### Set up virtualenvwrapper

In your shell initialisation file (eg. ~/.bashrc), add two lines like this:

    export WORKON_HOME=$HOME/.virtualenvs
    source /usr/local/bin/virtualenvwrapper.sh

(Change the path to virtualenvwrapper.sh depending on where it was installed.  For instance, on Fedora it is installed at /usr/bin/virtualenvwrapper.sh.)

WORKON_HOME is a directory where virtualenvwrapper is going to collect the virtualenvs that you use it to create. 

virtualenvwrapper provides the following commands:

```console
mkvirtualenv TDD
rmvirtualenv TDD
workon TDD # activate the virtualenv called foo
deactivate # whatever the currently active virtualenv is
```

A full list of commands is at
[http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html](http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html)

### Use pip to install To-Do list dependencies

```console
pip install -r requirements.txt
```
Make sure your virtualenv is activated when you run this command, then pip will only install these packages for this virtualenv.