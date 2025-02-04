# Git Notes

## Working with git locally
- 'git init' : initialize current folder as a git repository
- 'git clone <URL>': brings the git repo from <URL> to current folder
- 'git status': tells us what we need to know about our repository

- 'git add <FILE>': adds <FILE> to the staging area
- 'git commit': open a text editor to write commit message
- 'git commit -m "MESSAGE"': writes MESSAGE as a commit without a text editor

- 'git log': shows the log (history) of our commits
- 'git log --oneline': shows the shorter oneline commit

- 'git diff': compare current uncommited state with last known git state
- 'git diff --staged': runs get diff between the staging area and last known state
- 'git diff HEAD~<NUMBER>": compares HEAD with commit <NUMBER> ago (relative)
- 'git diff <HASH>': compares HEAD with the commit in <HASH>

- 'git restore --source <HASH OR HEAD~> <FILE>': restore file to <HASH OR HEAD~>"
- 'git checkout <HASH OR HEAD~>": if you forget the file, you end up in detached head
- 'git checkout master': go back to main
- 'git switch main': go back to main
- 'git checkout <HASH OR HEAD~> <FILE>': restores file to <HASH OR HEAD~>

## Working with remotes

- 'git remote add <NAME> <URL>': adds the <URL> as a remote with the name <NAME>

- 'git remove -v': look at': pushes what to where
- 'git remote rm <NAME>': removes remote called NAME 

- 'git pull <WHERE><WHAT>': pulls the <WHAT> branch in <WHERE> to local comupter


## Branches

- 'git branch <NAME>': create branch <NAME> where you are (HEAD)
- 'git switch <NAME>': move to the branch <NAME>
- 'git checkout <NAME>': also move to the branch <NAME>
- 'git switch -c <NAME>': create and move to the branch <NAME> in 1 command
- 'git checkout -b <NAME>': also create and move to branch <NAME> in 1 command

- 'git merge <BRANCH>': merge <BRANCH> into your current branch
- 'git rebase': command to change the history of a commit
- 'git rebase <BRANCH>': incorporate changes from <BRANCH> into current branch

- commits from 'git merge' can be automaitcally combined

- 'git status': is your friend
- 'git add <FILE>': to mark conflict resolution
- 'git rebase --continue': move to next commit in rebase
- 'git rebase --abort': undo git rebase step

- 'git rebase -i <COMMIT> HEAD~ or <HASH>': go into interactive rebase
- you can make multiple commit changes here, e.g., 'squash'/'s'
- 'git rebase -i <HASH>^': use ^ to include that commit in interactive rebase

- 'git stash' or 'git commit': to save work before moving branches
- 'stash' is temporary
- 'git stash list': see your stashed commits
- 'git stash apply': apply your last stashed commit
- 'git stash clear': clean up your stashes

- a 'merge' on the remote is called a "pull request" or "merge request"
--'git push <WHERE> <WHAT>'
- to update a PR, we make the changes to the branch locally and re-push


- a merge conflict can happen after a PR is issued
- 'git fetch': update your git log without making any changes to your files
- 'git fetch --prune': update your log and remove deleted remote branches

- 'git push -f <WHERE> <WHAT>': force push to the remote <WHERE> the branch <WHAT>
- 'git push --force-with-lease <WHERE> <WHAT>': more mindful of collaborators

## Collaborators

- add collaborators in repository settings
- collaborators will then 'git clone <URL>' to get repo on their computer
