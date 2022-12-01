#Starting a project
git clone <SSH URL from Github>
touch <filename>
cd <directory + TAB>
cd - <to go back>
ls

#Updating, statis, add files, commit
git status
git add . 
git commit -m "message"
git push

#others

##start git to listen to changes
git init 

##for non-online folder, connects to a web 
git remote add origin <SSH or HTTP URL>

##sets current local branch as main
git branch -M main

##pushes code to <remote> <from this branch>
git push -u origin main

##checkout switches branch, -b makes new branch, test is the name of the new branch
git checkout -b test

##check all existing branches
git branch

##merge the <branch> named test with the main
git merge test


#one command updating
##steps
To use nano, in your terminal, type nano ~/.bashrc
Then press Ctrl + w +v to go to the end, add what you want to add, the Ctrl + o to save changes, Ctrl +x to exit. You will need to log out and log back on, or run source ~/.profile to make your changes available to your bash environment.
Add this line

    function lazygit() {
        git add .
        git commit -a -m "$1"
        git push
    }

Call the command

    lazygit "My commit msg"

