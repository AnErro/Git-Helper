# Git-Helper
Note form of the Learn Some Git Nitwits presentation.
##What is git?

- version control
- its great for dummies like me
- This is Evernote turning my notes on Git into a presentation so if it is wordy don’t worry about it

##TL;DR Concepts:

- Staging Area: A place(kinda) where we can group files together before we "commit" them to Git.
- Pull: is a fancy way combining the git fetch  and the git merge  commands
- Fetch: gets all commits from a branch but it is easier to just see it as a synch command
- Fork: not a command or anything it is just a term for making a clone of the main repo on both your local machine and a server that you plan to edit, change, and probably break.
- Push: usual takes what you have on your ‘branch’ and merges it with the main version
- Commit: A "commit" is a snapshot of our repository. This way if we ever need to look back at the changes we've made (or if someone else does), we will see a nice timeline of all changes.
- Branch: is just an environment that starts as a new version of the current branch your in (usually the master branch), so that you can test stuff there and take what works and move it back to the master branch.

##Basic commands:

- **git init**: makes what ever directory you are in a repo
- **git add**: makes git start tracking a file
    - 👏 wildcards i.e. git add ‘*.txt’ : mind the quotes it adds everything
- **git commit -m _“something that describes your change here"_**
- **git stash** : for times when you love your changes but you don’t want to commit to them because what if something else comes up you want to be free! (i.e. you have commitment issues) It just puts your changes that you made to a stack that you can call on later to come back
- **git clone [url]**: basically just makes a local copy of the repo
- **git diff** : show differences from commits
- **git log**: shows a log commits

##git status: tells you what is actually happening in your git directory. What has been added what hasn't

- When you run it you get to see all of these types of files
- staged: Files are ready to be committed.
- unstaged: Files with changes that have not been prepared to be committed.
- untracked: Files aren't tracked by Git yet. This usually indicates a newly created file.
- deleted: File has been deleted and is waiting to be removed from Git.

##git add: sets a file to staged

- **add all**: You can also type git add -A . where the dot stands for the current directory, so everything in and beneath it is added. The -A ensures even file deletions are included.
- **git reset**: You can use git reset <filename> to remove a file or files from the staging area.

##Branches

- **git branch [name]**: Makes a new branch
- **git checkout [name]**: Turns your git directory to the last commit of the branch
- **git push [alias] [branch]**:update a remote repository with the changes you've made locally
   - It will take what your **[branch]** looks like and push it to be [branch] on the remote, if possible. If someone else has pushed since you last fetched and merged, the Git server will deny your push until you are up to date.

##OH NO, Someone pushed changes to the master branch and now you can’t merge your branch with the master branch!
     Steps to over come this tragedy

- remain calm
- **git fetch [alias]** : This just gets all changes to [alias]  (keep in mind this can be a remote repo too)
- **git merge [alias] / [branch]** : The slash is needed, example is git merge upstream/master  would sync up your fork (master) and the OG repo [alias]

##What about all this remote non sense?

- **git remote** : lists all remote repos aliases
- **git remote -v** : lists all remote repos, with urls listed with push/pull abilities
- **git remote add [alias] [url]** : self explanatory git remote add origin www.url.com/gitrepo
- **git pull [remote branch] [local branch]** : take changes from remote repo

"Push" is you forcing the changes being present in the target repository. "Pull" is the target repository grabbing your changes to be present there.
     A "pull request" is you requesting the target repository to please grab your changes.
     A "push request" would be the target repository requesting you to push your changes.

##Useful links

- http://gitref.org/index.html
- https://try.github.io
- https://help.github.com/articles/syncing-a-fork/

