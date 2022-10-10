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