# Git Project

Here are the series of Git Bundle exersise

``` bash
PS C:\Users\UZI\Desktop\Exercise> git init
Initialized empty Git repository in C:/Users/UZI/Desktop/Exercise/.git/
PS C:\Users\UZI\Desktop\Exercise> git add .
PS C:\Users\UZI\Desktop\Exercise> git status
On branch main
No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

PS C:\Users\UZI\Desktop\Exercise> git commit -m "My first commit"
[main (root-commit) 39cc212] My first commit
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
PS C:\Users\UZI\Desktop\Exercise> git remote add origin git@github.com:rubaju/Exersise-Git.git
>>
Counting objects: 100% (3/3), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 275 bytes | 91.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:rubaju/Exersise-Git.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\UZI\Desktop\Exercise> git push
PS C:\Users\UZI\Desktop\Exercise> git checkout -b dev
PS C:\Users\UZI\Desktop\Exercise> git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/rubaju/Exersise-Git/pull/new/dev
remote:
To github.com:rubaju/Exersise-Git.git
PS C:\Users\UZI\Desktop\Exercise> git checkout -b test
PS C:\Users\UZI\Desktop\Exercise> git push origin test
remote:
remote:      https://github.com/rubaju/Exersise-Git/pull/new/test
remote:
To github.com:rubaju/Exersise-Git.git
 * [new branch]      test -> test
PS C:\Users\UZI\Desktop\Exercise> git checkout dev
Switched to branch 'dev'
PS C:\Users\UZI\Desktop\Exercise> git origin --delete test
git: 'origin' is not a git command. See 'git --help'.
PS C:\Users\UZI\Desktop\Exercise> git status
On branch dev
Untracked files:
        home.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\UZI\Desktop\Exercise> git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

PS C:\Users\UZI\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 39cc212 My first commit
PS C:\Users\UZI\Desktop\Exercise> git status
On branch dev
Untracked files:
        about.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\UZI\Desktop\Exercise> git add about.html
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\UZI\Desktop\Exercise> git stash
PS C:\Users\UZI\Desktop\Exercise> git stash list
stash@{1}: WIP on dev: 39cc212 My first commit
PS C:\Users\UZI\Desktop\Exercise> git add team.html
PS C:\Users\UZI\Desktop\Exercise> git status
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\UZI\Desktop\Exercise> git stash
Saved working directory and index state WIP on dev: 39cc212 My first commit
stash@{1}: WIP on dev: 39cc212 My first commit
PS C:\Users\UZI\Desktop\Exercise> git stash pop
On branch dev
Changes to be committed:
        new file:   team.html

Dropped refs/stash@{0} (658923bd53f157a37a010427f6a88e48b7a1055f)
PS C:\Users\UZI\Desktop\Exercise> git add team.html
PS C:\Users\UZI\Desktop\Exercise> git stash 
Saved working directory and index state WIP on dev: 39cc212 My first commit
stash@{0}: WIP on dev: 39cc212 My first commit
stash@{1}: WIP on dev: 39cc212 My first commit
stash@{2}: WIP on dev: 39cc212 My first commit
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

stash@{0}: WIP on dev: 39cc212 My first commit
stash@{1}: WIP on dev: 39cc212 My first commit
stash@{2}: WIP on dev: 39cc212 My first commit
PS C:\Users\UZI\Desktop\Exercise> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    --index               attempt to recreate the index

PS C:\Users\UZI\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 39cc212 My first commit
stash@{1}: WIP on dev: 39cc212 My first commit
stash@{2}: WIP on dev: 39cc212 My first commit
PS C:\Users\UZI\Desktop\Exercise> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\UZI\Desktop\Exercise> git add .
PS C:\Users\UZI\Desktop\Exercise> git commit -m "Setup my home and about page"
On branch dev
nothing to commit, working tree clean
PS C:\Users\UZI\Desktop\Exercise> 

```