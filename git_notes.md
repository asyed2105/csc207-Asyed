# Git commands

### git status <br>
- show modified files in working directory, staged for your next commit <br>
- will say which branch we are on <br>
- will say "changes not staged for commit" this means that we did not tell git to look/do anything with it yet <br>

### git add [file]<br>
- add a file as it looks now to your next commit (stage)<br>
    - you are telling git this file is iMpOrTaNt it will pay attention to it now <br>
      - IF you now call *git status*, it will say "changes to be committed" <br>
        - will say modified:   [file] <br>
    - YOU CAN ALSO WRITE FILE_PATH RATHER THAN NAME! <br>

### git commit -m “[descriptive message]” <br>
- commit your file and add a description for your new commit  <br>
- every time you commit you are making a new version of your file <br>
-  will say after how many file chnages and insertions <br>
    - eg: 1 file changed, 1 insertion(+) <br>
    -  after if you call *git status*, it will say "Your branch is ahead  of "origin/main" by 1 commit <br>
            - origin/main <br>
                - our file on our actual github <br>
                - origin is where the file we are working with is from <br>
        - will tell you to use *git push* to publish yor local commits to actual github <br>

### git push <br>
-  publish yor local commits to actual github <br>

### git branch 'name of new branch' <br>
- makes a new branch <br>

### git log <br>
- can see all the commits/changes made n<br>

### git checkout 'name of new branch' <br>
- switches you to another branch to work out of <br>

## ** AFTER YOU MAKE CHANGES TO YOUR FILES AND WANT TO UPDATE YOUR REPO***: <br>
- git add file_name<br>
- git commit -m "pushing"<br>
- git push<br>

***
- you can make changes on another branch
- then go back on main and merge the changes you make on the new branch to the main branch

eg.
git checkout -b new_branch_name
-- make edits --
git add file_name
git commit -m "trying"
git checkout main
git merge new_branch_name

