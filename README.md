# git-for-teams demo

This is a sample readme so that I can demonstrate how to work and commit with a branching/merging strategy.

This is a commit to master after the branch has been taken.

## Basic workflow

1. Begin to work a feature in a branch taken from master
- Once your current work is done from your branch do a final commit.
- running a `git status` at this point should show 'nothing to commit, working directory clean' message.
- perform a `git checkout master`
- perform a `git pull origin master` <- this gets everything from master to your local machine.  Things may have changed and you need to have all the code currently in master locally to move forward.
- perform a `git checkout <whatever branch you were just working on>`
- Now Merge!  `get merge master` <- this commands allows you to bring any changes that have been made in master since you took your branch into your working branch.
- You _**might**_ have merge conflicts at this point.  Follow what git is telling you at the command line. You will have to hand edit the files it tells you have conflicts.  If you aren't sure which files have merge conflicts do another `git status` or do a find in your project for chevrons `<<<`.  
- _**Important!**_  once all files that had merge conflicts are edited, run your specs and do a quick run through your app to make sure nothing broke.  If something broke, resolve it.
- Commit your files to your working branch.
- Push your branch
- Do your pull request of your branch to master.
