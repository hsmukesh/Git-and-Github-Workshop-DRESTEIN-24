# Git-and-Github-Workshop-DRESTEIN-24
NAME:  MUKESH HS

REGISTER NUMBER : 212222060155  

DEPARTMENT :  ECE

YEAR :  3rd

Git and GitHub Workshop Assignment 

Complete the following tasks to practice core Git commands. Answer each question and perform the associated Git operations. 

1. Setup and Initialize: 
-	What command do you use to create a new directory named git-workshop and navigate into it? 

Answer:

To create a new directory named git-workshop and navigate into it, you can use the following commands in a terminal:

bash

mkdir git-workshop

cd git-workshop

 -mkdir git-workshop creates the new directory.
 
 - cd git-workshop changes the current directory to git-workshop.

2. Initialize a Git Repository: 
-	What command initializes a Git repository in your directory? 

Answer:

To initialize a Git repository in your directory, use the following command:

bash

git init

This command sets up a new Git repository in the current directory, creating a .git subdirectory that contains all the necessary files for version control.

3. Create and Modify Files: 
-	How do you create a new file named hello.txt and add the content 'Hello, Git Workshop!' to it using a single command? 

Answer:

You can create a new file named hello.txt and add the content "Hello, Git Workshop!" to it using the following command:

Bash

echo "Hello, Git Workshop!" > hello.txt

This command uses echo to output the text and redirects (>) it into a new file called hello.txt. If hello.txt already exists, this command will overwrite its content.

4. Check the Status of Your Repository: 
-	What command displays the status of your repository? 

Answer:

To display the status of your Git repository, use the following command:

bash

git status

This command shows the current state of the repository, including any changes that have been staged, changes that are not staged, and any untracked files.

5. Stage and Commit Changes: 
-	What command stages the file hello.txt?  
-	What command commits the staged file with the message 'Add hello.txt with welcome message'? 
Answer:

To stage the file hello.txt, use the following command:

bash

git add hello.txt

This command adds hello.txt to the staging area.

To commit the staged file with the message "Add hello.txt with welcome message," use the following command:

bash

git commit -m "Add hello.txt with welcome message"

This command creates a commit containing the changes made to hello.txt along with the provided commit message.

6. Branching: 
-	What command creates a new branch named update-content? 
-	How do you switch to the update-content branch? 

Answer:

To create a new branch named update-content, use the following command:

bash

git branch update-content

To switch to the update-content branch, use this command:

bash

git checkout update-content

Alternatively, you can create and switch to the new branch in a single command using:

bash

git checkout -b update-content

This command creates the update-content branch and immediately switches to it.

7. Make Changes on the Branch: 
-	What command would you use to append the text 'This is a simple Git assignment.' to hello.txt? 
-	What command stages and commits the changes with the message 'Update hello.txt with additional message'? 
Answer:

To append the text "This is a simple Git assignment." to hello.txt, you can use the following command:

bash

echo "This is a simple Git assignment." >> hello.txt

This command uses echo to output the text and appends it (>>) to the end of hello.txt.

Next, to stage the changes and commit them with the message "Update hello.txt with additional message," use the following commands:

First, stage the changes:

bash

git add hello.txt

Then, commit the changes with the message:

bash

git commit -m "Update hello.txt with additional message"

This will stage and commit your changes accordingly.

8. Merge Changes: 
-	What command switches you back to the main branch? 
-	How do you merge the update-content branch into main? 

Answer:

To switch back to the main branch, use the following command:

bash

git checkout main

Once you're on the main branch, you can merge the update-content branch into main using the following command:

bash

git merge update-content

This command merges the changes from the update-content branch into the current branch (which should be main).

2.	View Commit History: 
-	What command shows the commit history? 

Answer:

To view the commit history of your Git repository, use the following command:

bash

git log

This command displays a list of commits in reverse chronological order, showing the commit hash, author, date, and commit message for each commit. You can also use various options with git log to customize the output, such as --oneline for a simplified view.

10. Undo and Reset (Practice Safely): 
-	If you make a change to hello.txt that you want to revert before committing, what command would you use? 
-	How can you reset your branch to a previous commit (optional, for advanced practice)? 

Answer:

If you make a change to hello.txt that you want to revert before committing, you can use the following command to discard the changes:

bash

git checkout -- hello.txt

This command restores hello.txt to the last committed state, effectively undoing any uncommitted changes.

### Resetting Your Branch to a Previous Commit

If you want to reset your branch to a previous commit (be cautious, as this can alter your commit history), you can use the following command, replacing <commit-hash> with the hash of the commit you want to reset to:

bash

git reset --hard <commit-hash>

This command will reset the current branch to the specified commit, removing all commits made after that point, as well as any changes in the working directory. 

If you want to keep your changes (unstaged) while resetting the commit history, you can use:

bash

git reset --soft <commit-hash>

This option keeps your changes in the staging area so you can re-commit them if needed.

11. Push to a Remote Repository (Optional):
-	What command adds a remote repository named origin? 
What command pushes your local main branch to the remote repository?

Answer:

To add a remote repository named origin, use the following command, replacing <repository-url> with the URL of your remote repository:

bash

git remote add origin <repository-url>

This command establishes a connection between your local repository and the remote repository referred to as origin.

To push your local main branch to the remote repository, use the following command:

bash

git push origin main

This command uploads the commits from your local main branch to the main branch on the remote repository named origin. If it's the first push, you might also need to set the upstream branch with:

bash

git push -u origin main

This sets the origin/main as the default upstream branch for future pushes and pulls.
