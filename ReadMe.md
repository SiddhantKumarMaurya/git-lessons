#### Git
- Version history for code
- download: git-scm.com/downloads
- Remember that "git add" doesn't actually create a new version it just lets us pick which changes we want in the next version.
- So to create a new version we're going to use another git command which is "git commit -m"
- **version = commit**
- **Why we create versions in git manually? Why is it not done automatically as in the case of google docs?**
- **Ans. The problem with codes is that untill you finish your code it probably doesn't work so we don't really want to be automatically creating versions of our code that doesn't work. For google docs it doesn't really matter if the thing's finished or not, it's just a bunch of words and sentences. So you're not going to get errors from a half finished document. That's not the same with half finished code. So that's why we always create versions manually with git we want to make sure that a code is good to go before we put it in our version history.**

- command "git log" only shows the current commit as well as the commits behind the current commit, but not any commits in front of it. So in order to show all of the commits in our version history, we use the command "git log --all"
- when we run the command "git checkout <hash|branch>" the head move to the selected branch or version
- When we run the command "git checkout <hash|branch> file" or "git checkout <hash|branch> folder/" or "git checkout <hash|branch> ." the files that we are viewing at the moment gets restored to the selected version but the head does not move.

- git repository: folder that is being tracked by git
- GitHub: specifically designed for git repositories
- Besides GitHub there are Bitbucket and GitLab.

- **Local Repository**: local = refers to things on our computer
- **Remote Repository**: remote = refers to things that are online
- **Push**: Upload to GitHub
- **Pull**: Download from GitHub
- git push only pushes **commits** up to our remote repository, so it only pushes commits up to GitHub. If your changes are not in a commit, then git push won't be pushing anything. So, even if we do "git add ."  and we add these changes to our staging area. Even if we run git push at that time, you'll notice that because these changes are not in a commit, remember that git only picks which  changes we want in a commit, it doesn't actually create a commit. If these changes are not in commit, git push will not push anything. git push only pushes commits.

- when we cloned our GitHub repository into a folder and made some commit and pushed it to GitHub repository, the current git repository and GitHub repository were in sync, but the original git repository that was created (after which the GitHub repository was created) was not in sync with the GitHub repository. Besides running the command "git log --all --graph" it showed the that it is in sync with the previous version (the version that got updated later by another local repository). It does not show the new commit that has been made by the another local repository. The this happens is because **remote tracking branches don't update automatically**. To reflect the changes we need to run the command: "git fetch", this command updates the result shown by "git log --all --graph"

- to make the local repository = remote repository run the command: "git pull <remote_name> master", in our case we had remote name set to "origin"

- SSH (secure shell or secure socket shell) key.

- When we merge two branches together the results will go on to the branch that we are currently working on (it will go on to the top).

- **Merge Conflict**:
	- A merge conflict in Git occurs when two or more branches have changes in 	the same part of a file, and Git cannot automatically merge them. This 	happens when:

	1. Two branches modify the same line(s) in a file.
	2. One branch deletes a file that another branch modifies.

	Git stops the merge process and marks the conflict in the file, allowing 	you to manually resolve it. Once resolved, you can complete the merge.

- What are feature branches?
1. A workflow.
2. A step-by-step process for using Git and GitHub.

- Feature Branch Workflow
1. Create a feature branch
2. Upload feature branch to GitHub
3. Create a "Pull Request" (do code reviews)
4. Merge feature branch into master/main branch (merge happens on GitHub)

---
#### Notes:
1. command `git add .`: adds only the current diretory for staging. If you want to stage changes made above the current directory then either traverse to that directory and write the command `git add .` or in the current directory write the command `git add <directory path>`.
