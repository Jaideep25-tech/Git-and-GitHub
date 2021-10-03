![](https://github.com/Jaideep25-tech/Git-and-GitHub/blob/main/assets/git%20commands.gif)

DIRECTORY
cd </file/path/code> -> change directory to a project

INITIALIZING
1. git init -> initialize an empty git repository

STATUS CHECK
2. git status -> list of files changed & those which needs to be staged or commit

STAGING & UNSTAGING
3. git add <file-name> -> stage a changed file
4. git add . -> stage all changed files
5. git rm --cached <file-name> / git restore --staged <file> -> unstage a file

COMMIT
6. git commit -m "message" -> commit all staged files with a message
7. git commit -am "message" -> stage all the changed files and commit with a message

BRANCH
8. git branch -> lists all branches names
9. git branch <branch-name> -> creates a new branch
10. git branch -d <branch-name> -> deletes a branch
11. git checkout <branch-name> -> switch to a specific branch
12. git merge <branch-name> -> merge a branch with main/master branch

GITHUB
13. git remote -v -> list all remote repos
14. git remote add origin <github-https-link>.git -> connect local repo with a remote repo
15. git remote set-url origin <github-https-link>.git -> change a remote git repo

16. git stash -> store current work locally with unstaged/untracked files (only if it clash with remote repo)
17. git stash pop -> bring stashed work back to working directory

18. git pull -> get latest changes from remote repo to local repo
19. git push origin <branch-name> -> push committed changes to a purticular branch

20. git log -> show all logs/commits in remote repo
21. git log --oneline -> show all logs in one line

DELETING COMMIT
(don't forget to store all deleting commit id)
      
22. [ 
      git log --oneline -> copy commit id of a commit after which all the commits should be deleted
      git reset <paste-that-id> -> delete all commits after the provided commit id
      git log --oneline -> to check if commits are deleted
      git push origin <branch-name> -f -> forcefully delete commits in remote repo
    ]
    
RESTORE COMMIT
(only be done if that commit id is present)
      
23. [ 
      git cherry-pick <deleted-commit-id> -> restore all deleted commits before this commit
      git log --oneline -> to check if commits are restored
      git push origin <branch-name> -> push commits to remote repo
    ]

SYNC GITHUB FORK
(only if remote repo is forked)
      
24. [
      git remote -v -> show only forked repo
      git remote add origin <https-link-of-main-repo> -> add main repo as upstream
      git remote -v -> to check if main repo is added in upstream
      git fetch upstream -> fetch all changes from main repo
      git merge upstream/<branch-name> -> merge those changes to local repo
      git push origin <branch-name> -> push those changes to forked repo
    ]
