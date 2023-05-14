# 1st-step we create the directory 
```
mkdir git_practice
```
# 2ndstep (we run cmd ls which show all directorie)
```
Android  AndroidStudioProjects  Desktop  Documents  Downloads  git_practice  Music  Pictures  Public  snap  Templates  Videos
```

# 3rd-step
### we change the directory and goto the working directory(git_practice).
```
 cd git_practice
```
# 4th-step
### we initialize the git in git_practice project and he tracket the history of the project
## output:-
<pre>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/shubham/git_practice/.git/
</pre>

# 5th-step 
### create readme file in the project
```
shubham@shubham-Latitude-7480:~/git_practice$ touch readme.md
```

# 6th-step
### make a html file in the project using below command
```
shubham@shubham-Latitude-7480:~/git_practice$ touch index.html
```
# 7th-step
### wrtie some html code in index.html file and the check status.
# output:-
```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        readme.md

nothing added to commit but untracked files present (use "git add" to track)
```
### note:- 
<pre>
this above message show our index.html and readme.md file which are not added with git track property so that reason show these above message means it is untracketd file.
</pre>

# 8th step
## run command  git add . or git add index.html
### now all file goto staging area or we can individual add file in staging area.

# 9th step
## again we check the staus 
# output :-
```
shubham@shubham-Latitude-7480:~/git_practice$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html
        new file:   readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

```
# 10th-step 
## these step we commit the code means if final change in the code the we run these below command
```
git commit -m "first commit of commit"
```
# output:-
<pre>
[master (root-commit) d6d2b04] first commit of commit
 2 files changed, 75 insertions(+)
 create mode 100644 index.html
 create mode 100644 readme.md
</pre>


# 11th-step
## these step local git add to remote github server
```
git remote add origin git@github.com:w3villa-shubham-rai/git_command_practice.git
```
### now add local git and remote github server.


# 12th-step
## now we check the using below cmd conecttion are establish or not.

```
$ git remote -v
```
# ouput:-
<pre>
origin  git@github.com:w3villa-shubham-rai/git_command_practice.git (fetch)
origin  git@github.com:w3villa-shubham-rai/git_command_practice.git (push)
</pre>

# 13th step (in this step above file already in stageing area but we move the file in un satage area)

### check the status
```
git status
```
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
</pre>


# 14th step 
### in these step we move the file in stage area(particular or onr file). 
```
git restore readme.md  
```

# output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
</pre>


# 15th-step 
### in these step we implement the log command and check the history of of all commit.
```
git log
```
# output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git log
commit 82fa0c103a06c2547687bc59b859656f79c8c5ea (HEAD -> master)
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 16:52:51 2023 +0530

    third commit

commit 8e8b93d4252f802cbf258bc67ab87b6dee1d7de0
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 16:33:25 2023 +0530

    secand commit

commit d6d2b04e767b02fed59ee1e806a37cec0ee4933d
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 15:41:17 2023 +0530

    first commit of commit
(END)
</pre>

# 16th- step

## now we push the code on remote server or repository

```
git push origin master
```
# output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$  git push origin master
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (10/10), 2.36 KiB | 2.36 MiB/s, done.
Total 10 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To github.com:w3villa-shubham-rai/git_command_practice.git
 * [new branch]      master -> master
</pre>

# now check log 

### output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git log
commit 82fa0c103a06c2547687bc59b859656f79c8c5ea (HEAD -> master, origin/master)
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 16:52:51 2023 +0530

    third commit

commit 8e8b93d4252f802cbf258bc67ab87b6dee1d7de0
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 16:33:25 2023 +0530

    secand commit

commit d6d2b04e767b02fed59ee1e806a37cec0ee4933d
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 15:41:17 2023 +0530

    first commit of commit
(END)
</pre>

# 16th-step
## if want to remove the commit then we use below command(use starting 11 digit of commit hash)

```
$ git reset d6d2b04e767
```
# output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git reset d6d2b04e767
Unstaged changes after reset:
M       readme.md
</pre>

# 17-step 
### now check status then we find previous commit is removed and showing the file modified

```
git staus
```
# output:-
<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
</pre>

# check  log

```
$ git log
```
#output:-

<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git log
commit d6d2b04e767b02fed59ee1e806a37cec0ee4933d (HEAD -> master)
Author: Shubham Rai <shubham.rai@w3villa.com>
Date:   Sun May 14 15:41:17 2023 +0530

    first commit of commit
</pre>


# 18th-step(git reset)
## these command goto all file in unstge area

```
$ git reset
```
# output:-
<pre>
Unstaged changes after reset:
M       readme.md
</pre>

### note :- all file in unstaged area.

<pre>
shubham@shubham-Latitude-7480:~/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
</pre>

# 19th-step(reset hard) 
## reset --hard  it totally chanege the local area and clean the changes from workspace  it remove from  workspace and stageing  thearea.
```
$ git reset -hard;
```
# 20th-step  (force flag )
### note:- not work git push command than we use below command 
```
git push --force
```
# output:-

<pre>
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (13/13), 3.28 KiB | 1.64 MiB/s, done.
Total 13 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To github.com:w3villa-shubham-rai/git_command_practice.git
 + 82fa0c1...957e717 master -> master (forced update)
</pre>
