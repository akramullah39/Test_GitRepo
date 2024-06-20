# Test_GitRepo

#Commands for GIT

$ git --version ( to check whether GIT is installed)
$ git config --global user.name "Mohammed"
$ git config --global user.email "akram......"

$ git init (It will initialized a local repository and create a .GIT dir which will track the changes and ensure that there is no secret. Git init will create a git dir which will watch this repo)
Initialized empty Git repository in C:/Users/mullah/GIT/.git/
$ ls -la

vi calculator.sh
git status
git add calculator.sh (To keep a track of file for versioning git needs to know which file to keep track using 'git add')
git checkout <file name> (if we don't want to keep the changes)
git status
git commit -m "fist version"
git status
vim calculator.sh
git status
git diff (to see what is added)
git add calculator.sh
git status
git commit -m "Second ver"
git diff
git status
git log (to see the versions which we hv committed)
git log --pretty=format:"%h - %au, - %ae - %s"
cat calculator.sh
cat calculator.sh

$git reset --hard <commit ID> (To restore back to a particular version use the below command)
git reset --hard 1d96c41793531041a52c904b5541a6f80af5df1

==========================================================================================================================================================
>>How to share the code?
========================
Now we have a local copy to share with our peers we need to push it to a distributed systems like GitHub, self hosted Git or bitbucket. To put this code open to the org
$git push (to push the code to GitHub for peers review)

CREATE A NEW REPOSITORY (CHATAPP)
$ git remote add origin https://github.com/akramullah39/ChatApp.git (adding a new repo in your git hub)
$ git remote -v
origin  https://github.com/akramullah39/ChatApp.git (fetch)
origin  https://github.com/akramullah39/ChatApp.git (push)

$ git push origin master -u (to push the local repo to remote repo)

>How to create a diff br?
When we want to add huge changes we don't make changes in the MAIN br or existing code/functionality. Instead we will create a new br for the new functionality and test.
GIT Branching Strategy:
=======================
Customer should receive release periodically
For this we need Git Branching

>>What is a Branch? Branch is a separation. If we require/want to make a breaking change to our existing code than we will create a Branch and test the changes by this way this will not effect existing functionality. After successful testing we will merge the branch to MAIN and deliver to customer.

Master br
Feature br
release br. In order to deliver the code to the customer we will not start from MASTER but we will deliver this changes from RELEASE branch.

$git branch
$git checkout -b <br name'division'>(create a br from the existing code)
$git checkout main (it will switch to Main br)
$git log (it will not show the newly added features in branch 'division' as we are in the MASTER br.)
$git log division (it will show all the versions)
$git checkout division && git log (it will switched to br 'division' and sh ver)

To merge the branches:
git merge
git rebase
git cherry-pick (easiest but good for 2-5 commits)

