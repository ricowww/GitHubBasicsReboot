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

