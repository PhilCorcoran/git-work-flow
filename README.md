# git-work-flow

Demonstrates what happens in a typical development workflow using [Vincent Driessen's branching model.](http://nvie.com/posts/a-successful-git-branching-model/) Distinguishes between what occurs on the server and what happens on the developer's PC. Assumes a central server with a management interface like github or gitlab. Uses the example of a shopping web site.
Describes the development process in 3 stages
##1. Setup repository
Create the repository and the feature branches. Initialize the repository with a `README.md`. Everything happens on the server here.

![alt text](images/gitflow1.jpg "Stage 1. Setup repo")
##2. Develop
Developers create branches, code and merge

![alt text](images/gitflow2.jpg "Stage 2. Developing")
##3. Release
Release preparation is begun. Developers submit major bug fixes. Final production release is merged into `master` branch and tagged.

![alt text](images/gitflow3.jpg "Stage 3. Releasing")