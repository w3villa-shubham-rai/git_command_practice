# first step we create the directory 
```
mkdir git_practice
```
# and secand step we run cmd ls which show all directorie
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


