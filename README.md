# Data Team Challenge

## Problem

![Don't insert to nested sets](https://robsite.net/wp-content/uploads/2012/03/3oc0f8.jpeg)

Not familiar with nested sets? Read [this](http://mikehillyer.com/articles/managing-hierarchical-data-in-mysql/).

With the switch to event streams, we will switch to calculating the nested sets on the fly on our side as opposed to receiving
them in full from the source every time a change is made.

## Requirements

1) Read full `test.tree` table into a program. Calculate the lft and rgt values for the nested sets.
Result should match the lft and rgt values in the `test.tree` table.
2) Add a node to the tree. Relcalculate the nested sets.
3) Move a node within the tree. Relcalculate the nested sets.
4) App must be implemented in NodeJS

## Competition

Consideration will be given to the following for scoring:

1) Correctness of the nested sets
2) Average Speed of execution over multiple iterations
3) Use of proper idiomatic patterns in NodeJS
    * Promises
    * async/await
    * Dependency Injection
    * Testability
    * Linting (standard is nice)
4) Unit Tests
5) Enforced automated linting / tests when committing code

A strawman folder for an node project running within docker

* Folder `src/` contains the node application.
* Folder `docker/` contains the docker build bits, with support for multiple environments in each sub folder
* The launch script for dev is `docker/{env}/app/launch`
* The `./local` command is a useful wrapper for docker-compose.  It prints out what it is running, so you can adjust to suite your needs.  You can get a full syntax by just running the command `./local`

## Developing

Run the app container:

    ./local dev up

### Connecting a shell

You can connect a shell to your running service with:

	./local dev sh

### Running a command against the docker container

    ./local dev sh -c "echo hello"
