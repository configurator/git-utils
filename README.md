# git-utils

This repository started its way as a fork of [`ddollar/git-utils`](http://github.com/ddollar/git-utils). Some of the utilities here are from there, others are my own creation, some loosely based on ddollar's versions.

### Installation

Simply clone this repository, and put it in your path. Make sure bash considers the `git-*` files executable.

_Note:_ All commands assume you are using a terminal and tools that supports ANSI color; if they are redirected, ANSI color is preserved. Some command line tools, such as `less`, support this with command line flags, but other tools, especially editors, may have a problem with that. If you are using these commands and redirecting output, I suggest using something like [strip-ansi](https://www.npmjs.com/package/strip-ansi) to remove these color codes.

### Utilities

Command             | Description
--------------------|----------------------------------------------------
`git newbranch`     | Creates a new branch, checks it out, and pushes the current state to the remote server, setting upstream tracking
`git addremove`     | Adds added files, removes deleted files
`git last`          | Simple alias for `git log`; shows the last few commits (defaults to 1, accepts a number for different number of commits)
`git meta`          | Simple alias for `git show`; shows metadata for a commit without the diff file
`git tree`          | Shows a graph of the repository's commits, branches and merges
`git my-tree`       | The same as `git tree`, except limited to commits by the current user (identified by email)
`git orphans`       | Shows a graph, like `git tree`, but includes all orphaned commits, e.g. once that have already been rebased
`git incoming`      | Shows incoming changes (this doesn't contact the server, so it's recommended to use `git fetch` first)
`git outgoing`      | Shows outgoing changes (which would be pushed to a remote server with `git push`)
`git rstatus`       | Shows complete status as compared to the origin (or other specified remote branch)
`git sync`          | Performs a pull, merge/rebase, then a push. Can stash unsaved changes and pop afterwords
`git srebase`       | Performs an interactive rebase, stashing (and popping afterwards) if there are any local changes

### Screenshots

###### `git tree`

![git-tree](https://raw.githubusercontent.com/configurator/git-utils/screenshots/git-tree.png)

###### `git orphans`

![git-orphans](https://raw.githubusercontent.com/configurator/git-utils/screenshots/git-orphans.png)

###### `git rstatus`

![git-rstatus](https://raw.githubusercontent.com/configurator/git-utils/screenshots/git-rstatus.png)
