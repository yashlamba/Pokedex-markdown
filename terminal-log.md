erikishiru@computer:~/Desktop$ cd Pokedex-markdown/
erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown\$ git branch

- master
  erikishiru@computer:~/Desktop/Pokedex-markdown$ git pull
dAlready up-to-date.
erikishiru@computer:~/Desktop/Pokedex-markdown$ git fetch upstream
  fatal: 'upstream' does not appear to be a git repository
  fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
erikishiru@computer:~/Desktop/Pokedex-markdown$ git remote
origin
erikishiru@computer:~/Desktop/Pokedex-markdown$ clear

erikishiru@computer:~/Desktop/Pokedex-markdown$ git remote
origin
erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown$ git checkout darkrai
error: pathspec 'darkrai' did not match any file(s) known to git.
erikishiru@computer:~/Desktop/Pokedex-markdown$ git checkout -b darkrai
Switched to a new branch 'darkrai'
erikishiru@computer:~/Desktop/Pokedex-markdown\$ git statu
git: 'statu' is not a git command. See 'git --help'.

Did you mean one of these?
status
stage
stash
erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch darkrai
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown$ code .
erikishiru@computer:~/Desktop/Pokedex-markdown\$ git status
On branch darkrai
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

    modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
erikishiru@computer:~/Desktop/Pokedex-markdown$ git add README.md 
erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch darkrai
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)

    modified:   README.md

erikishiru@computer:~/Desktop/Pokedex-markdown$ git commit -m "Added Darkrai"
[darkrai 23c366e] Added Darkrai
 1 file changed, 8 insertions(+), 6 deletions(-)
 rewrite README.md (97%)
erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch darkrai
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown\$ git push
warning: push.default is unset; its implicit value has changed in
Git 2.0 from 'matching' to 'simple'. To squelch this message
and maintain the traditional behavior, use:

git config --global push.default matching

To squelch this message and adopt the new behavior now, use:

git config --global push.default simple

When push.default is set to 'matching', git will push local branches
to the remote branches that already exist with the same name.

Since Git 2.0, Git defaults to the more conservative 'simple'
behavior, which only pushes the current branch to the corresponding
remote branch that 'git pull' uses to update the current branch.

See 'git help config' and search for 'push.default' for further information.
(the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
'current' instead of 'simple' if you sometimes use older versions of Git)

fatal: The current branch darkrai has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin darkrai

erikishiru@computer:~/Desktop/Pokedex-markdown\$ git push --set-upstream origin darkrai
Username for 'https://github.com': erikishiru
Password for 'https://erikishiru@github.com':
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 500 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'darkrai' on GitHub by visiting:
remote: https://github.com/Erikishiru/Pokedex-markdown/pull/new/darkrai
remote:
To https://github.com/Erikishiru/Pokedex-markdown.git

- [new branch] darkrai -> darkrai
  Branch darkrai set up to track remote branch darkrai from origin.
  erikishiru@computer:~/Desktop/Pokedex-markdown$ git remote add upstream https://github.com/yashlamba/Pokedex-markdown
erikishiru@computer:~/Desktop/Pokedex-markdown$ git checkout master
  Switched to branch 'master'
  Your branch is up-to-date with 'origin/master'.
  erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown$ git fetch upstream
  remote: Enumerating objects: 101, done.
  remote: Counting objects: 100% (101/101), done.
  remote: Compressing objects: 100% (43/43), done.
  remote: Total 95 (delta 29), reused 83 (delta 22), pack-reused 0
  Unpacking objects: 100% (95/95), done.
  From https://github.com/yashlamba/Pokedex-markdown
- [new branch] master -> upstream/master
  erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown$ git rebase upstream/master
  First, rewinding head to replay your work on top of it...
  Fast-forwarded master to upstream/master.
  erikishiru@computer:~/Desktop/Pokedex-markdown$ git status
On branch master
Your branch is ahead of 'origin/master' by 35 commits.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean
erikishiru@computer:~/Desktop/Pokedex-markdown$ git push
  warning: push.default is unset; its implicit value has changed in
  Git 2.0 from 'matching' to 'simple'. To squelch this message
  and maintain the traditional behavior, use:

git config --global push.default matching

To squelch this message and adopt the new behavior now, use:

git config --global push.default simple

When push.default is set to 'matching', git will push local branches
to the remote branches that already exist with the same name.

Since Git 2.0, Git defaults to the more conservative 'simple'
behavior, which only pushes the current branch to the corresponding
remote branch that 'git pull' uses to update the current branch.

See 'git help config' and search for 'push.default' for further information.
(the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
'current' instead of 'simple' if you sometimes use older versions of Git)

Username for 'https://github.com': erikishiru
Password for 'https://erikishiru@github.com':
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/Erikishiru/Pokedex-markdown.git
cc778ee..a947fb0 master -> master
erikishiru@computer:~/Desktop/Pokedex-markdown$ LS 
The program 'LS' is currently not installed. You can install it by typing:
sudo apt install sl
erikishiru@computer:~/Desktop/Pokedex-markdown$ LS
The program 'LS' is currently not installed. You can install it by typing:
sudo apt install sl
