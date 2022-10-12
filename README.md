# GIT Exercise

## Bundle 1

### Exercise 1

```bash
TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1
$ >>> git init
    Initialized empty Git repository in 
    C:/Users/TheGym/Desktop/Git/bundle1/.git/
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (master)

$>>> git branch -m Main
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git add README.md
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git commit -m "add readme"
    [Main (root-commit) 1145a98] add readme
    1 file changed, 0 insertions(+), 0 deletions(-)
    create mode 100644 README.md
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git remote add orgin https://github.com/hirwaaldo1/git-exercises.git
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git status
    On branch Main
    nothing to commit, working tree clean
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)
$>>> git push
    fatal: The current branch Main has no upstream branch.        
    To push the current branch and set the remote as upstream, use
        git push --set-upstream orgin Main
    To have this happen automatically for branches without a tracking
    upstream, see 'push.autoSetupRemote' in 'git help config'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git push --set-upstream orgin Main
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 206 bytes | 206.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    To https://github.com/hirwaaldo1/git-exercises.git
    * [new branch]      Main -> Main
    branch 'Main' set up to track 'orgin/Main'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)
    $ git cheackout -b dev
    git: 'cheackout' is not a git command. See 'git --help'.
    The most similar command is
            checkout
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (Main)

$>>> git checkout -b dev
    Switched to a new branch 'dev'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
    $ git status
    On branch dev
    nothing to commit, working tree clean
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git push orgin dev
    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
    remote: 
    remote: Create a pull request for 'dev' on GitHub by visiting:
    remote:      https://github.com/hirwaaldo1/git-exercises/pull/new/dev
    remote:
    To https://github.com/hirwaaldo1/git-exercises.git
    * [new branch]      dev -> dev
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
    Switched to a new branch 'test'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (test)


$>>> git push orgin test
    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
    remote:
    remote: Create a pull request for 'test' on GitHub by visiting:
    remote:      https://github.com/hirwaaldo1/git-exercises/pull/new/test
    remote:
    To https://github.com/hirwaaldo1/git-exercises.git
    * [new branch]      test -> test
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (test)

$>>> git branch -d test
    error: Cannot delete branch 'test' checked out at 'C:/Users/TheGym/Desktop/Git/bundle1'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (test)

$>>> git checkout dev
    Switched to branch 'dev'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git branch -d test
    Deleted branch test (was 1145a98).
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git push orgin --delete test
    To https://github.com/hirwaaldo1/git-exercises.git
    - [deleted]         test
````

### Exercise 2
```` bash
TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
$ git stash list
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
    $>>> git add home.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash 
    Saved working directory and index state WIP on dev: 1145a98 add readme
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git add about.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash
    Saved working directory and index state WIP on dev: 1145a98 add readme
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git add team.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)


$>>> git stash
    Saved working directory and index state WIP on dev: 1145a98 add readme
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash pop stash@{1}
    On branch dev
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            new file:   about.html
    Dropped stash@{1} (02049c4a8baf9a0a7ce9ccfdbd75a5fb3c72b1a3)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash pop stash@{1}
    On branch dev
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            new file:   about.html
            new file:   home.html
    Dropped stash@{1} (9bdded39b76b1809555b632fb13142c61127ad09)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git commit add --all
    fatal: paths 'add ...' with -a does not make sense
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git  add --all
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git commit -m "about page and home page"
    [dev 77fc96d] about page and home page
    2 files changed, 24 insertions(+)
    create mode 100644 about.html
    create mode 100644 home.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git push
    fatal: The current branch dev has no upstream branch.
    To push the current branch and set the remote as upstream, use
        git push --set-upstream orgin dev
    To have this happen automatically for branches without a tracking
    upstream, see 'push.autoSetupRemote' in 'git help config'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git push --set-upstream orgin dev
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (4/4), done.
    Writing objects: 100% (4/4), 541 bytes | 270.00 KiB/s, done.
    Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), done.
    To https://github.com/hirwaaldo1/git-exercises.git
    1145a98..77fc96d  dev -> dev
    branch 'dev' set up to track 'orgin/dev'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash list
    stash@{0}: WIP on dev: 1145a98 add readme
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git stash pop
    On branch dev
    Your branch is up to date with 'orgin/dev'.
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            new file:   team.html
    Dropped refs/stash@{0} (9d4da386673a011158df1517f6100e6eee72a644)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git reset --hard
    HEAD is now at 77fc96d about page and home page
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)

$>>> git status
    On branch dev
    Your branch is up to date with 'orgin/dev'.
    nothing to commit, working tree clean
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
````

## Bundle 2

### Exercise 1
```` bash
TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (dev)
$>>> git checkout -b ft/bundle-2 
    Switched to a new branch 'ft/bundle-2'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)
    $ git add service.html
    fatal: pathspec 'service.html' did not match any files
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)

$>>> git add services.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)
    $ git status
    On branch ft/bundle-2
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            new file:   services.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)

$>>> git commit -m "bundle-2 execres-1"
    [ft/bundle-2 8a862f8] bundle-2 execres-1
    1 file changed, 12 insertions(+)
    create mode 100644 services.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)
    $ git push
    fatal: The current branch ft/bundle-2 has no upstream branch.
    To push the current branch and set the remote as upstream, use
        git push --set-upstream orgin ft/bundle-2
    To have this happen automatically for branches without a tracking
    upstream, see 'push.autoSetupRemote' in 'git help config'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)

$>>> git push --set-upstream orgin ft/bundle-2
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 460 bytes | 230.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: 
    remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
    remote:      https://github.com/hirwaaldo1/git-exercises/pull/new/ft/bundle-2
    remote:
    To https://github.com/hirwaaldo1/git-exercises.git
    * [new branch]      ft/bundle-2 -> ft/bundle-2
    branch 'ft/bundle-2' set up to track 'orgin/ft/bundle-2'.
````


### Exercise 2

```` bash

TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/bundle-2)
$>>> git checkout main
    Switched to branch 'main'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
$>>> git pull
    remote: Enumerating objects: 1, done.
    remote: Counting objects: 100% (1/1), done.
    remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (1/1), 623 bytes | 155.00 KiB/s, done.
    From https://github.com/hirwaaldo1/git-exercises
    * [new branch]      main       -> orgin/main
    There is no tracking information for the current branch.
    Please specify which branch you want to merge with.
    See git-pull(1) for details.
        git pull <remote> <branch>
    If you wish to set tracking information for this branch you can do so with:
        git branch --set-upstream-to=orgin/<branch> main
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)

$>>> git checkout main
Switched to branch 'main'
TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)

$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=orgin/<branch> main


$>>> git checkout -b ft/service-redesign
    Switched to a new branch 'ft/service-redesign'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)
    $ git checkout main
    Switched to branch 'main'
    M       services.html
    Your branch is up to date with 'orgin/main'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
$>>> git add --all
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
    $ git checkout -b ft/service-redesign
    fatal: a branch named 'ft/service-redesign' already exists
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)

$>>> git checkout  ft/service-redesign
    Switched to branch 'ft/service-redesign'
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)

$>>> git add --all
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)
    $ git commit -m "feat:adding changes on service.html"
    [ft/service-redesign f988d57] feat:adding changes on service.html
    1 file changed, 2 insertions(+), 2 deletions(-)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)
    $ git push
    fatal: The current branch ft/service-redesign has no upstream branch.
    To push the current branch and set the remote as upstream, use
        git push --set-upstream orgin ft/service-redesign
    To have this happen automatically for branches without a tracking
    upstream, see 'push.autoSetupRemote' in 'git help config'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)

$ git push --set-upstream orgin ft/service-redesign
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 308 bytes | 308.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    remote: 
    remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
    remote:      https://github.com/hirwaaldo1/git-exercises/pull/new/ft/service-redesign
    remote:
    To https://github.com/hirwaaldo1/git-exercises.git
    * [new branch]      ft/service-redesign -> ft/service-redesign
    branch 'ft/service-redesign' set up to track 'orgin/ft/service-redesign'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)
    $ git checkout main
    Switched to branch 'main'
    Your branch is up to date with 'orgin/main'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
    $ git add --all
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)

$>>> git commit -m "feat:add old service"
    [main 6b35c93] feat:add old service
    1 file changed, 2 insertions(+), 2 deletions(-)
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
    $ git push
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 294 bytes | 294.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    To https://github.com/hirwaaldo1/git-exercises.git
    de83fc2..6b35c93  main -> main
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (main)
    $ git checkout  ft/service-redesign
    Switched to branch 'ft/service-redesign'
    Your branch is up to date with 'orgin/ft/service-redesign'.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign)

$>>> git merge main
    Auto-merging services.html
    CONFLICT (content): Merge conflict in services.html
    Automatic merge failed; fix conflicts and then commit the result.
    # with '#' will be ignored, and an empty message aborts the commit.
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign|MERGING)

$>>> git add service.html
fatal: pathspec 'service.html' did not match any files
TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign|MERGING)

$ git add services.html
    TheGym@DESKTOP-9BO2974 MINGW64 ~/Desktop/Git/bundle1 (ft/service-redesign|MERGING)
$>>> git commit
    [ft/service-redesign 73f53f6] Merge branch 'main' into ft/service-redesign