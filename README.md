
fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab
$ git init
Initialized empty Git repository in C:/Users/fs/Desktop/selab/.git/

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (master)
$ notepad file1.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (master)
$ git checkout -b b1
Switched to a new branch 'b1'

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (b1)
$ notepad file2.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (b1)
$ notepad file3.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (b1)
$ git status
On branch b1

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file1.txt
        file2.txt
        file3.txt

nothing added to commit but untracked files present (use "git add" to track)

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (b1)
$ git branch -M main

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git commit -m "First commit"
On branch main

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file1.txt
        file2.txt
        file3.txt

nothing added to commit but untracked files present (use "git add" to track)

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git branch --all

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git checkout -
error: pathspec '-' did not match any file(s) known to git

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git checkout
fatal: You are on a branch yet to be born

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git checkout -b part
Switched to a new branch 'part'

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git branch --all

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git log
fatal: your current branch 'part' does not have any commits yet

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git commit -m "First commit"
On branch part

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file1.txt
        file2.txt
        file3.txt

nothing added to commit but untracked files present (use "git add" to track)

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git status
On branch part

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file1.txt
        file2.txt
        file3.txt

nothing added to commit but untracked files present (use "git add" to track)

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git add .

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git status
On branch part

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file1.txt
        new file:   file2.txt
        new file:   file3.txt


fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git commit -m "Second commit"
[part (root-commit) 7581038] Second commit
 3 files changed, 3 insertions(+)
 create mode 100644 file1.txt
 create mode 100644 file2.txt
 create mode 100644 file3.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git log
commit 7581038520bab49766e5ebc522ed38a2ec36936a (HEAD -> part)
Author: parthivvan <parthivvanapalli@gmail.com>
Date:   Tue Aug 5 11:57:25 2025 +0530

    Second commit

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git remote add origin https://github.com/parthivvan/SE

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/parthivvan/SE'

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ ^C

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git push -u origin part
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 370 bytes | 21.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'part' on GitHub by visiting:
remote:      https://github.com/parthivvan/SE/pull/new/part
remote:
To https://github.com/parthivvan/SE
 * [new branch]      part -> part
branch 'part' set up to track 'origin/part'.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (part)
$ git branch -m main
git push -u origin main
To https://github.com/parthivvan/SE
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/parthivvan/SE'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ ^C

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git push -u origin main --force
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/parthivvan/SE
 + 72fcc88...7581038 main -> main (forced update)
branch 'main' set up to track 'origin/main'.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ ^C

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git checkout -b feature
Switched to a new branch 'feature'

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ notepad f1

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ notepad f2

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git push -u origin main
branch 'main' set up to track 'origin/main'.
Everything up-to-date

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ ^C

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git push -u origin feature
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'feature' on GitHub by visiting:
remote:      https://github.com/parthivvan/SE/pull/new/feature
remote:
To https://github.com/parthivvan/SE
 * [new branch]      feature -> feature
branch 'feature' set up to track 'origin/feature'.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git push -u origin feature --force
branch 'feature' set up to track 'origin/feature'.
Everything up-to-date

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git add .

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git commit -m feature
[feature 7dfdc13] feature
 2 files changed, 2 insertions(+)
 create mode 100644 f1.txt
 create mode 100644 f2.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git push -u origin feature --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 367 bytes | 367.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/parthivvan/SE
   7581038..7dfdc13  feature -> feature
branch 'feature' set up to track 'origin/feature'.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git pull origin main
From https://github.com/parthivvan/SE
 * branch            main       -> FETCH_HEAD
Already up to date.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git merge feature
Already up to date.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git push -u origin feature --force
branch 'feature' set up to track 'origin/feature'.
Everything up-to-date

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (feature)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git pull origin main
From https://github.com/parthivvan/SE
 * branch            main       -> FETCH_HEAD
Already up to date.

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git merge feature
Updating 7581038..7dfdc13
Fast-forward
 f1.txt | 1 +
 f2.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 f1.txt
 create mode 100644 f2.txt

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$ git push -u origin feature --force
branch 'feature' set up to track 'origin/feature'.
Everything up-to-date

fs@DESKTOP-GGREQK6 MINGW64 ~/Desktop/selab (main)
$
