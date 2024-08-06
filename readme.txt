Initializing a Git repository
the first step is to initialize a Git repository. 

    Open Git Bash.

    Navigate to the root directory of your project.

    Initialize the EMPTY  local directory as a Git repository. By default, the initial branch is called main.

    If you’re using Git 2.28.0 or a later version, you can set the name of the default branch using -b.

    git init -b main

    Add the files in your new local repository. This stages them for the first commit.

    $ git add .
    # Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.

    Commit the files that you've staged in your local repository.

    $ git commit -m "First commit"
    # Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.



    Adding a local repository to GitHub using Git

Before you can add your local repository to GitHub using Git, you must authenticate to GitHub on the command line. For more information, see "About authentication to GitHub."

    Create a new repository on GitHub.com. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub. For more information, see "Creating a new repository."

    At the top of your repository on GitHub.com's Quick Setup page, click 

    to copy the remote repository URL. for example, it will be:

    https://github.com/antondrroid/test_new_local_repository.git

    Screenshot of the "Quick Setup" header in a repository. Next to the remote URL, an icon of two overlapping squares is highlighted with an orange outline.

    Open Git Bash.

    Change the current working directory to your local project.

    To add the URL for the remote repository where your local repository will be pushed, run the following command. Replace REMOTE-URL with the repository's full URL on GitHub.

    git remote add origin https://github.com/antondrroid/test_new_local_repository.git

    For more information, see "Managing remote repositories."

    To verify that you set the remote URL correctly, run the following command.

    git remote -v

answer must be looks like:

            PS D:\projects_old\test_new_local_repository> git remote -v
            origin  https://github.com/antondrroid/test_new_local_repository.git (fetch)
            origin  https://github.com/antondrroid/test_new_local_repository.git (push)

    To push the changes in your local repository to GitHub.com, run the following command.

    git push origin main
if not work, try 
          git push origin
if say:
fatal: The current branch ain has no upstream branch.
To push the current branch and set the remote as upstream, use
       
        git push --set-upstream origin ain

    If your default branch is not named "main," replace "main" with the name of your default branch. For more information, see "About branches."

Further reading

    "Adding a file to a repository"
    "Troubleshooting the 2 GB push limit"


