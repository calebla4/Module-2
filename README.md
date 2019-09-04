# Module 2 Homework: Getting up and running with GitHub.

**Instructions**

1. Make an account! Follow [these instructions](https://happygitwithr.com/github-acct.html).
2. Check to see if Git is already installed on your computer. Note that this will require you to work from the shell. I recommend launching the [shell from RStudio](https://happygitwithr.com/shell.html#shell) by going to *Tools > Shell*. From there, follow [these steps](https://happygitwithr.com/install-git.html). **If you have Windows**, be sure to change your RStudio settings such that the shell opens with Git Bash, as described [under A.3.1](https://happygitwithr.com/shell.html#shell).
3. [Introduce yourself to Git from the shell](https://happygitwithr.com/hello-git.html).
4. Fork this repository (`BAE-R-Coding/Module-2`) to your own. Note that the `Fork` button is off to the right of the name of this repository (the one you're looking at right now). Once you fork the repository, you will have created a copy of it on your GitHub account. You should automatically be navigated to the forked repository on your GitHub account.
5. Create a project in RStudio using the ["Existing project, Github first"](https://happygitwithr.com/existing-github-first.html#existing-github-first) workflow (you only need to go through step 16.2). By creating a project in RStudio from a GitHub repository, you are cloning the GitHub repository to your computer.  

- **Note:** To get the URL of your forked GitHub repository, click on the green `Clone or download` button on your repository's GitHub page. `Clone with HTTPS` should then pop up - copy the link shown there. If the pop up opens with `Clone with SSH`, just click the "Clone with HTTPS" link in blue (also located in the pop up). The link should be something like: `https://github.com/your_GitHub_username/Module-2.git`.  

![](img/forked-repo.png){width=400px}

- **One more note:** When you are creating the project, do not change the project directory name. The project directory name will automatically populate once you enter the link to your forked repository. You can, however, place your repository in any directory on your computer using `Browse...`.  

![](img/rproj-git-repo.png){width=400px}

6. Your RStudio project should now be open. In the File pane of the RStudio window, you should see the files from the GitHub repository. When you created the project in RStudio, you should have specified where the project would live on your computer (i.e., the directory path, which you may have selected using "Browse"). The GitHub repository was cloned to this location on your computer. Go find it and confirm it's where you expect it to be.
7. Now, we need to tell Git that there is an "upstream" version of this repository (i.e., the original repository that you forked is the "upstream" version). To do this, open the shell from RStudio (*Tools > Shell*) and enter `git remote add upstream https://github.com/BAE-R-Coding/Module-2.git`. Note that you are entering https://github.com/BAE-R-Coding/Module-2.git because you are telling Git there the upstream GitHub repository is located, which is on the BAE-R-Coding account. 
8. In the shell, enter `git remote -v`. You should see 4 lines: two that begin with "origin" and two that begin with "upstream".
9. Create a branch, which is a parallel version of the repository. When you create a branch, you're essentially creating a version of your files that you can freely edit. To create a branch, enter `git checkout -b my-branch master` in the shell. "my-branch" will be the name of this new branch you're creating. In the shell, you should see `Switched to a new branch my-branch`. 
10. In RStudio, click on the `Git` tab in the top-right pane. Near the top-right of this pane, you should see `my-branch`, which signals that RStudio knows you are working from the new branch you just created.
11. Navigate to your Files pane. Click on `Module-2-raleigh-rainfall.R` to open it. It should open in the script editor pane. With this script, you will retrieve Raleigh weather data for 2019 and evaluate how much rainfall we've received thus far this year. Go ahead and run the individual lines/sections of code. **At the bottom of the code**, type your answer to the question. Save the script. When you save the script, you should notice that the file name of the script pops up in your Git tab on RStudio. This is because you've made a change to the file, and Git is tracking your changes.
12. In the Git tab, check off all  boxes under 'Staged'. Each line corresponds to a set of changes that were made to files in your project directory. Once you've checked the boxes, click the `Commit` button. A new window will open. In this window, click on `Module-2-raleigh-rainfall.R`. In the bottom half of the pane, you'll see the changes you made to the file (i.e., where you typed your answer to the question). In the top right of this window, you can enter a commit message. Go ahead and type a few words, something like "Answered question" or "Found wettest month in 2019". Then click `Commit`. A new window will pop up; close it, and also close the commit window. You have now committed your changes! 
13. Next, you need to *push* your commit to your remote repository (that is, the cloud-based GitHub repository). Open up the shell. Enter `git push origin my-branch`. 
14. Go to your repository on your GitHub page. Click on the green button that says `Compare & pull request`. You are now going to submit a *pull request*, which is how you propose changes to the original repository you forked. If you were collaborating with a fellow coder on a project, you would submit the pull request to propose modifications to her or his code. In this case, you are going to submit a pull request to let me know that you have completed the assignment. Please title your pull request with your name, and include a brief message (something like "Assignment completed"). If you want to confirm you sent your pull request, you can navigate to https://github.com/BAE-R-Coding/Module-2/pulls.
15. Return to your GitHub repository's webpage. Note that you can see your commit message next to files that were updated, and the length of time since you submitted your commit (e.g., 10 minutes ago). Click on the link for `Module-2-raleigh-rainfall.R`. Here, you'll see your updated code. Click on `History` and then click on the hyperlinked commit message you most recently submitted. Here, you can see your diffs, or how your file changed in the most recent revision. 

References:
- [Happy Git and GitHub for the useR](https://happygitwithr.com/), Jenny Bryan, Jim Hester, and STAT545 TAs.
- [An introduction to Git and how to use it with RStudio](https://r-bio.github.io/intro-git-rstudio/), R Programming for Biologists. 
