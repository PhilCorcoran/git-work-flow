# git-work-flow

Demonstrates what happens in a typical development workflow using [Vincent Driessen's branching model.](http://nvie.com/posts/a-successful-git-branching-model/) Distinguishes between what occurs on the server and what happens on the developer's PC. Assumes a central server with a management interface like github or gitlab. Uses the example of a shopping web site.
Describes the development process in 3 stages
##1. Setup repository
Create the repository and the feature branches. Initialize the repository with a `README.md`. Everything happens on the server here.
![alt text](images/gitflow1.jpg "Stage 1. Setup repo")
[Full size image](https://raw.githubusercontent.com/PhilCorcoran/git-work-flow/master/images/gitflow1.jpg)
##2. Develop
Developers Tom &amp; Jerry create branches, write code and merge

![alt text](images/gitflow2.jpg "Stage 2. Developing")
[Full size image](https://raw.githubusercontent.com/PhilCorcoran/git-work-flow/master/images/gitflow2.jpg)
##3. Release
Release preparation is begun. Developers submit major bug fixes. Final production release is merged into `master` branch and tagged.

![alt text](images/gitflow3.jpg "Stage 3. Releasing")
[Full size image](https://raw.githubusercontent.com/PhilCorcoran/git-work-flow/master/images/gitflow3.jpg)

## Commands
The following commands are used during the workflow. Any word prefixed with `$` is a variable such as the url of the git repository `$git_repo_url`

| Command                                            | Where            |
|:---------------------------------------------------|:-----------------|
| git clone $git_repo_url --branch $branch           | remote --> local |
| git remote -v update                               | remote --> local |
| git status                                         | local            |
| git merge $working_branch -m $merge_commit_message | local            |
| git checkout $branch -b $new_branch                | local            |
| git branch -rv                                     | remote           |
| git add -A                                         | local            |
| git commit -m $commit_message                      | local            |
| git log                                            | local            |
| git log $remote_repo/$remote_branch                | remote           |
| git show $commit_hash                              | local            |
| git diff origin/$branch                            | remote & local   |
| git pull origin $branch                            | remote --> local |
| git push origin                                    | local--> remote  |
| git checkout $release_branch -b $local_branch      | local            |
| git push origin --tags                             | local --> remote |
| git tag -l                                         | local            |
| git reset --hard origin/master                     | remote --> local |

