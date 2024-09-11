## Git commands

git status 
-> show modified files in working directory, staged for your next commit
--> will say which branch we are on
-> will say "changes not staged for commit" this means that we did not tell git to look/do anything with it yet

git add [file]
-> add a file as it looks now to your next commit (stage)
    -> you are telling git this file is iMpOrTaNt it will pay attention to it now 
    -> IF you now call *git status*, it will say "changes to be committed"
        -> will say modified:   [file]

git commit -m “[descriptive message]”
-> commit your file and add a description for your new commit 
-> every time you commit you are making a new version of your file
-> will say after how many file chnages and insertions 
    -> eg: 1 file changed, 1 insertion(+)
    -> after if you call *git status*, it will say "Your branch is ahead  of "origin/main" by 1 commit 
            -> origin/main
                --> our file on our actual github
                --> origin is where the file we are working with is from
        -> will tell you to use *git push* to publish yor local commits to actual github

git push
->  publish yor local commits to actual github

git branch 'name of new branch'
-> makes a new branch

git log
-> can see all the commits/changes made


git checkout 'name of new branch'
-> switches you to another branch to work out of
            
