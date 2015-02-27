# Computational Materials database

## Requirements
  
The computational material's database needs to connect to a MongoDB instance as database backend.
You can obtain a copy at [MongoDB](http://www.mongodb.org).
You will also need the python MongoDB driver `pymongo`, which should be installed automatically.
If not try `pip install pymongo` to install the package.

The package requires Python 3 and is tested with version 3.3.

## Installation

    git clone git@bitbucket.org:glotzer/compmatdb.git
    cd compmatdb
    python setup.py install

On system's without root access you can install the package with
  
    python setup.py install --user

into your home directory.

## Testing

To check if the package was installed correctly, execute `import compdb` within a python shell.
That should not result in any error.

To test the package, executing `nosetests` within the repositories root directory.
Most tests require a MongoDB instance to be available on localhost on the standard port.

## Setting up a project.

The database facilitates a project-based workflow.
This is how you set up a new empty project.

    mkdir my_project
    cd my_project
    compdb init MyProject

This will create the basic configuration for a project named "MyProject" within the directory `my_project`.
In addition, a few example scripts will be created, that may, but do not have to be the starting point for the creation of new project routines.

To test if everything is correctly setup, you can then execute `python run.py` which will run a mock parameter exploration study without actually storing any data.

## More examples

Less minimal boilerplate scripts can be obtained with:

    compdb init MyProject --template example

In addition to the minimal template scripts, this will actually store data within your project database, which can be analyzed.
These scripts are provided to be slightly more exemplary on how to use the package.