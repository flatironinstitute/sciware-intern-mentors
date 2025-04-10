# Examples of efficient workflows

## Branches

Branches are one of the most important features of a mature and active project.
Start by having a branch, often just called `main` that represents a "working" version.
Any new development, for example adding new functionality, trying to optimize an existing piece, can be done on a separate "feature" branch.
These branches will then often turn into Pull Requests (see ...).

## CI, Github actions

Github has a builtin CI (Continuous Integration testing) that allows you to run "actions" that automatically run tests on your code.
If you have a test suite, even a simple one, you can setup Github to run this test suite on every commit.
Example...

## Documentation, web pages

You can also use github to host [Github Pages](https://pages.github.com/).
This is a good place to host information about your project, such as documentation.
These are created by putting web pages on a special branch called `gh-pages`.

## Useful views

You can see a lot on Github just by browsing through the code, but there are a number of different views into the code and its history that can be confusing.
Just clicking through the file list will let you see the current state of the files, often with syntax highlighting and fancy search functionality by clicking on function names.

