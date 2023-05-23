## Technical

1. What is `Git`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is a very famous tool which facilitates source code management in software development.
- We can track changes in computer files (versions) using `Git`.
- Using git can track the progress of a project over time as well as coordinate work among team developers.
</blockquote> 

</details>

---
2. What is the difference between `Git` and `GitHub`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is a version control tool, used to manage the history of changes performed to source code.
- Whereas `GitHub` is a web application that provides service to host source code, commonly referred to as Git repository.
- `GitHub` provides all of the distributed version control and `source code management (SCM)` functionalities of Git, along with a few of its features.
  
</blockquote> 
    
</details>

---
3. What do you understand by Git repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Git repository refers to a folder/location where all the Git files are stored.
- These files can either be stored on the local repository or the remote repository.
- The local repository is the folder inside your system where you will find one hidden folder named `.git` 

</blockquote> 

</details>

---

4. What do you mean by initializing a repository in Git? How do we do it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Usually, when a new project is created, developers first initialize the local repository using `Git` on their system.
- Initializing a repository in Git means creating a directory that will start tracking the changes to your files or source code.
- To do this, we first create a simple empty directory for our application and execute the below command using Git-

```
git init
```

- After the above command, a hidden `.git` folder will appear in the directory.
</blockquote> 

</details>

---

5. Can we modify the `.git` hidden folder under any Git repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Ideally, the contents of the  .git folder are modified by the `git` command, we are not supposed to tamper with any files manually.
- The .git folder contains all information that is necessary for the project and all information relating to commits, remote repository address, etc. 
- It also contains a log that stores the commit history and helps to roll back to the desired version of the code.
</blockquote> 

</details>

---

6. How to view commit logs in git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Git repository holds all of the commits (snapshots of all your files at a point in time) that have been made. 
- We can access the commit history with the below command.

```
git log
```

</blockquote> 

</details>

---

7. What is the working directory/tree in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The project files that we are currently working on are called working trees,or working directory
- We can think of a working tree as a file system where you can view and modify files.
  
</blockquote> 

</details>

---

8. What is the staging area in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The staging area also called an index, is where commits are prepared. 
- The index compares the files in the working tree to the files in the repo. 
- When you make a change in the working tree, the index marks the file as modified before it is committed.
  
</blockquote> 

</details>

---

9. How to copy the remote repository onto your local machine?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- We can copy a remote repository onto your local machine using the below command

```
git clone '<remote-repository-url>'
```

-  Above command will automatically set up a local master/main branch that tracks the remote master/main branch it was cloned from.
</blockquote> 

</details>

---

10. How to clone a specific branch using `git clone` command?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- To clone lets say feature branch named `feature/audit` from the GitHub remote repository we can use the below command-

```bash
git clone -b feature/audit --single-branch 'https://<github-username>@github.com/my-organization/my-project.git'
```

</blockquote> 

</details>

---

11. Which command adds a change from the working directory to the staging area.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `git add` command adds a change in the working directory to the staging area. 
- We tell Git that we want to include updates to a particular file in the next commit. 

```
git add -A 
or 
git add --all
```

-  Above command stages all (new, modified, deleted) files
</blockquote> 

</details>

---

12. What is the Git command to save your changes to the local repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `git commit` command is used to save your changes to the local repository.
- We need to ensure that we use the `git add` command to mark the desired changes for inclusion. 

```
git commit -m "Added first commit"
```

-  In the above command, we specify the message for the commit.

</blockquote> 
</details>

---

13. What is the use of the `git push` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `git push` command is used to upload local repository content to a remote repository. 
- Using this command we transfer commits from your local repository to a remote repo.

```
git push 
```

</blockquote> 
</details>

---

14. What are untracked files in git status?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Untracked files are files that have been created within your repo's working directory but have not yet been added to the repository's tracking index using the `git add command.
  
</blockquote> 

</details>

---

15. What is a source code repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A source-code repository is an archive with the code as well as the hosting facility for these software archives, where you can also have the project’s technical documentation, web pages, snippets, patches, etc. which can be accessed publicly (open-source) or privately.

</blockquote>

</details>

---

16.  What are the benefits of the source code repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 


Using a source code repository has many potential benefits for an organization, including:

- **Concurrent Development:** Repositories usually allow multiple developers to make edits to different parts of the same program simultaneously. Developers can then merge their changes back into the main program.
- **Increased Transparency:** Most source code repositories require a developer to check out, edit, and then check back in the part of the program he or she was editing. The repository records which developer made changes and when, resulting in a log of updates made to the program over time.
- **Version Control:** When developers make enough changes to a program stored in a source code repository, they can designate the updated program as a new “version” of the software. A repository also stores previous versions of a program, a feature that allows companies to restore a previous version if, for example, an update introduces a harmful bug.

</blockquote>

</details>

---

17. What are some basic Gitlab commands?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

1. Git init
2. Git add
3. Git commit
4. Git status
5. Git config
6. Git branch
7. Git checkout
8. Git merge

</blockquote>

</details>

---

18. How do you solve merge conflict?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><b>Show Answer</b></summary>

<blockquote>

A merge confilct can be resolved in three ways:

1. Keep only the other branch's changes/Accepting the incomming changes 
2. Keep only your branch's/Accepting the current changes
3. Make a brand new change, which may incorporate changes from both branches


- markers `<<<<<<<`, `=======`, `>>>>>>>` should me removed.
- If there are multiple merge conflicts in a  single file make sure to resolve all of them.
- After resolving all the cconflicts `mark as resolved` can be clicked.

</blockquote>

</details>

---

19. List some of the commands in git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><b>Show Answer</b></summary>

<blockquote>

Few commonly used git commands are:

- **`git config`:** It is used to configure the options like name, email etc. 

- **`git help`:** If you get stuck anywhere in git or if you need any information about any git command, git help provides detailed information about git commands.

- **`git init`:** Used to initialize a git repository.

- **`git add`:**Git add is used to add the changes made in the working directory to the staging area.

- **`git stash`:** It is used to save all the stagged and unstagged changes.

- **`git commit`:** It is used to save the changes to the local repository.

- **`git status`:** It gives the state of the working directory and the staging area. Information about the current branch, stagged changes and un-stagged changes are displayed using git status.

- **`git push`:** It is used to upload the local repository content to the remote repository. 
</blockquote>
</details>

---
    
20. What commands do you need to upload code to github ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><b>Show Answer</b></summary>

<blockquote>

To update the changes to remote repository the follwing commands are used:

1. **`git add`:** Git add is used to add the changes made in the working directory to the staging area. 

```git
git add filename
```

To add multiple files that have the same extension, the following command is used.
```git
git add *.extention
```
For recursively adding all the changes to all files, the following command is used.

```git
git add .
```

2. **`git commit`:** Git commit is used to save the changes to the local repository.

```git
git commit -m "message"
```
3. **`git push`:** git push is used to upload the local repository content to the remote repository. After committing all the changes, the following command is implemented to push the changes to the remote repository.

```git
git push
```

</blockquote>

</details>

---

21. What protection policies would you put in place on a branch?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To protect a branch in Git, you can set up branch protection policies. Some common protection policies include:

1. Requiring pull requests to merge changes into the branch.
2. Requiring a minimum number of reviewers to approve changes before they can be merged.
3. Disabling force pushes to the branch.
4. Requiring a passing build status before changes can be merged.
5. Enforcing code review standards, such as requiring certain checks to pass before changes can be merged.

</blockquote> 

</details>

---

22. How would you avoid overriding main code (Git)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To avoid overriding main code in Git, you can follow these steps:

1. Always create a new branch when making changes.
2. Work on the new branch and commit changes regularly.
3. Use pull requests to merge changes into the main branch.
4. Before merging, make sure to review the changes and resolve any conflicts.
5. Make sure to test changes thoroughly before merging them into the main branch.

</blockquote> 

</details>

---

23. How do you create a pull request in GitHub?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To create a pull request with GitHub, follow these steps:

1. Create a new branch from the main branch.
2. Make changes to the new branch and commit them.
3. Push the new branch to your remote repository.
4. On the GitHub website, navigate to the repository and select the new branch.
5. Click on the "New pull request" button.
6. Choose the main branch as the base branch and the new branch as the compare branch.
7. Add a title and description for the pull request.
8. Review the changes and resolve any conflicts.
9. Once everything looks good, click on the "Create pull request" button.

</blockquote> 

</details>

---

24. How did you do code reviews before merging?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Before merging code, code reviews are an important step to ensure quality and catch any errors. Some ways to do code reviews include:

1. Using a dedicated code review tool, such as Crucible or Review Board.
2. Using pull requests and reviewing changes on the GitHub website.
3. Using a collaborative code editor, such as Visual Studio Code or Atom, and reviewing changes in real-time.
4. Pair programming, where two developers work on the same code simultaneously and review each other's work.

</blockquote> 

</details>

---

25. What pattern did you follow for Git management?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

There are many patterns that can be followed for Git management, but one common pattern is the Gitflow workflow. In this pattern, development is done in feature branches that are merged into a develop branch. Releases are made from the develop branch, and hotfixes are done in separate branches that are merged into both the develop and master branches. The master branch always represents the latest production release.

</blockquote> 

</details>

---

26. What are the steps to setting up a Git repo?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The basic steps to set up a Git repository are as follows:

1. Create a new repository in a Git hosting service (such as GitHub, GitLab, or Bitbucket).
2. Clone the repository to your local machine using the `git clone` command.
3. Add files to the repository using the `git add` command.
4. Commit changes to the repository using the `git commit` command.
5. Push the changes to the remote repository using the `git push` command.

</blockquote> 

</details>

---

27. List the git repository hosting services.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

There are several popular Git repository hosting services, including:

1. GitHub
2. GitLab
3. Bitbucket
4. Azure DevOps
5. AWS CodeCommit
6. SourceForge

</blockquote> 

</details>

---

28. When using Git as version control, how would you merge a branch into main?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To merge a branch into main (or any other branch), follow these steps:

1. Switch to the branch you want to merge into (e.g., `main`) using the `git checkout` command.
2. Run the `git merge` command, followed by the name of the branch you want to merge (e.g., `git merge my-feature-branch`).
3. Resolve any merge conflicts that may occur.
4. Commit the merge changes using the `git commit` command.
5. Push the changes to the remote repository using the `git push` command.

</blockquote> 

</details>

---

29. "If both of us are working on the same file, how will you handle it so you would not delete/erase my updates?"

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To avoid overwriting each other's changes when working on the same file in Git, you can use branches. Each person can work on a separate branch and then merge their changes into the main branch when they're ready. Alternatively, you can use a pull request workflow, where one person submits their changes as a pull request and the other person reviews and approves the changes before merging them into the main branch.

If you both need to work on the same file simultaneously, you can use a version control system that supports locking, where only one person can make changes to the file at a time. However, this can be less efficient and more prone to conflicts than using branches or pull requests.

</blockquote> 

</details>

---

30. What is git flow, work flow? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

- Git flow is a branching model used in Git. 
- It is used to define a strict branching model designed around the project release. 
- Git flow consists of various branches, such as feature, release, and hotfix branches, to help manage the development process. 
- A typical Git flow workflow involves creating a feature branch from the develop branch, making changes to the feature branch, merging the feature branch back to the develop branch after testing, creating a release branch, and then merging the release branch into the master branch after testing.

 </blockquote> 

</details>

---

31. Explain Git and version control.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Git is a distributed version control system that allows developers to track changes made to the codebase and collaborate effectively with team members. It provides various features like branching, merging, and staging, which make it easy to manage code changes and collaborate effectively with team members. Git allows developers to work on a project locally and then push changes to a remote repository, which can be accessed by other team members.

</blockquote> 

</details>

---

32. What was the hardest part of git keeping ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The hardest part of Git keeping is resolving conflicts that arise when two or more team members make changes to the same file. Git provides various tools and features to help manage conflicts, such as merging, rebasing, and pull requests. However, conflicts can still occur, especially in large codebases with many contributors. Resolving conflicts requires careful attention to detail and good communication between team members. 
    
</blockquote> 

</details>

---

33. What's the most important things to consider when merging a pull request?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
When merging a pull request, it is important to consider the following things:

1. Review the changes made in the pull request to ensure they are in line with the project's requirements and coding standards.
2. Ensure that the pull request has been tested and does not introduce new bugs or break existing functionality.
3. Make sure that the pull request does not conflict with other changes in the codebase.
4. Communicate with the person who submitted the pull request to ensure that any concerns or questions are addressed before merging. 

</blockquote> 

</details>

---

34. Explain the difference between the Github master/head and development branches.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Git, the "master" branch is the default branch that contains the stable, production-ready code. The "head" branch refers to the most recent commit in a branch. The "development" branch, on the other hand, is a branch used for ongoing development work. It may contain code changes that are not yet ready for production, such as new features or bug fixes that are still being tested. The development branch is usually merged into the master branch once all changes have been tested and approved for production. 
    
</blockquote> 

</details>

---

35. If code does get overridden how would you go about fixing that?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

If code gets overridden in Git, there are several ways to fix it depending on the situation. 

One way is to use Git's "reflog" feature to find the commit that contained the original code and then revert the code back to that commit. 

Another way is to use Git's "rebase" command to rewrite the history of a branch and incorporate the original code changes into the current codebase. 

If the code was overwritten by mistake and the original code is lost, it may be possible to retrieve the code from a backup or from another team member who has a copy of the code. 
    
</blockquote> 

</details>

---

36. What is a pull request in GitHub?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

A pull request is a way to propose changes to a project's codebase and merge those changes into the main branch. Pull requests allow team members to review and discuss changes before they are merged into the main branch, which helps ensure that code changes are high quality and do not break existing functionality. 

</blockquote> 

</details>

---

37. List the tools used for project management.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

There are various tools available for project management, each offering different features and functionalities. The choice of tool depends on the specific needs and requirements of the project and the team using it. Here is a list of commonly used tools for project management:

- Trello
- Asana
- Jira
- Basecamp
- Microsoft Project
- Monday.com
- Smartsheet
- Wrike
- Teamwork
- Notion
    
</blockquote> 

</details>

---

38. What are the advantages and disadvantages of Version Control?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
The advantages of version control systems like Git include:

- Easy collaboration: Version control systems allow multiple developers to work on a project simultaneously and track changes made to the codebase.
- Code management: Version control systems provide features like branching, merging, and staging, which make it easy to manage code changes and keep track of different versions of a project.
- Error recovery: Version control systems provide tools to revert changes and recover lost code.

The disadvantages of version control systems include:

- Learning curve: Version control systems like Git can have a steep learning curve for beginners.
- Complexity: Large projects with many contributors can be complex to manage in a version control system.
- Conflict resolution: Conflicts can arise when multiple team members make changes to the same file, which can be challenging to resolve.

Overall, the benefits of using a version control system like Git usually outweigh the disadvantages. 

</blockquote> 

</details>

---

39. What is rebasing in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Rebasing in Git is a process where a developer moves the changes made in one branch to a different branch. The developer essentially applies the changes made in one branch on top of the other branch. This can be useful in scenarios where there are changes in one branch that the developer wants to include in another branch. Rebasing helps keep the commit history linear and clean, which can make it easier to understand the development process. 

</blockquote> 

</details>

---

40. What is the difference between SVN repository and Git repository?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The main difference between SVN (Subversion) and Git is that SVN is a centralized version control system, while Git is a distributed version control system. In SVN, all team members access a central repository, and changes made by each team member are merged back into this central repository. In Git, every team member has a local copy of the repository, and changes are synced between team members through pushing and pulling changes from a remote repository.

Another difference is that SVN tracks changes to individual files, while Git tracks changes to the entire codebase. Git provides better branching and merging capabilities than SVN, which makes it easier to manage code changes and collaborate effectively with team members. 

</blockquote> 

</details>

---

41. How do you create a new branch in Git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To create a new branch you need to use the following commands:
`git branch <branch-name>`
Replace `<branch-name>` with the desired name for your new branch. Avoid using spaces or special characters in the branch name. Using lowercase letters and hyphens or underscores to separate words is common practice.
ex: `git branch feature-branch`
Once you've created the branch, you can switch to it using the git checkout
`git checkout <branch-name>` ex: `git checkout feature-branch`

Alternatively, you can combine the branch creation and checkout steps into a single command using the -b flag, like this: `git checkout -b <branch-name>` ex: `git checkout -b feature-branch`

</blockquote> 

</details>

---

42. How do you switch between branches in Git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To switch to an existing branch, use the following command:
`git checkout <branch-name>` ex: `git checkout feature-branch`

</blockquote> 

</details>

---

43. How do you revert a commit in Git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

- To revert a commit in Git, you can use the git revert command. The git revert command creates a new commit that undoes the changes made in a previous commit. `Git revert <commit>`	Replace `<commit>` with the commit hash or reference of the commit you want to revert
- Git will open a text editor to enter a commit message for the revert. Modify the message if desired, save the file, and close the text editor. Alternatively, you can use the `-m` flag followed by a commit message to specify the revert message directly in the command, like this: `git revert -m "Reverting commit XYZ"`
- Git will create a new commit that undoes the changes made in the specified commit. This revert commit will be added to the branch you are currently on
- After reverting the commit, you can push the changes to a remote repository if necessary. Use the `git push` command to push the updated branch to the remote repository.

</blockquote> 

</details>

---

44. What is the purpose of the "git pull" command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The purpose of the git pull command is to fetch the latest changes from a remote repository and incorporate them into the current branch. It essentially combines two separate Git commands: git fetch and git merge.

</blockquote> 

</details>

---

45. What is the purpose of the "git fetch" command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The purpose of the git fetch command is to retrieve the latest commits, branches, and tags from a remote repository without merging them into your current branch. It allows you to fetch the updates from a remote repository and examine them before integrating them into your local branch.

</blockquote> 

</details>

---

46. What is the purpose of the ".gitignore" file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The purpose of the .gitignore file in a Git repository is to specify intentionally untracked files or directories that should be ignored by Git. It allows you to exclude certain files, file types, or entire directories from being tracked and committed to the repository.

</blockquote> 

</details>

---

47. How do you undo the last commit in Git without losing the changes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

- To undo the last commit in Git without losing the changes, you can use the `git reset` command along with the `--soft` option. This allows you to remove the commit from the branch history while keeping the changes in your working directory and staging area. To undo the last commit, use the following command:
`git reset --soft HEAD~1`
- To discard the changes altogether and start fresh, you can use the `git reset --hard HEAD~1` command instead. This command will remove the last commit, reset the branch pointer, and discard the changes from the last commit.

</blockquote> 

</details>

---

48. What is the purpose of the "git stash" command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The purpose of the git stash command is to save the current changes in your working directory and the staging area into a temporary area called the "stash." It allows you to set aside your unfinished changes so that you can switch branches, apply patches, or perform other operations without committing or losing your work.

</blockquote> 

</details>

---

49. What is the difference between a merge and a rebase in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Merge: Combines the changes from one branch into another, creating a new merge commit and preserving branch histories.

Rebase: Moves or combines commits from one branch onto another, rewriting the commit history to create a linear sequence without merge commits.

</blockquote> 

</details>

---

50. Explain the concept of Git branching strategies (e.g., GitFlow)

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Git branching strategies, such as GitFlow, provide guidelines for managing branches and organizing development workflows in Git. Git branching strategies define rules and conventions for creating, naming, and merging branches to facilitate collaboration and streamline development processes. One popular strategy is GitFlow, which involves the following branches: 

- Master: Represents the production-ready code, containing stable and thoroughly tested versions of the software.
- Develop: Acts as the main development branch where features are integrated. It should always be in a deployable state, but it may contain work in progress.
- Feature branches: Created off the develop branch for developing specific features or enhancements. Each feature branch is short-lived and should have a clear purpose. Once completed, the branch is merged back into the develop branch.
- Release branches: Created from the develop branch when preparing for a new release. These branches undergo final testing and bug fixes. Once ready, they are merged into both the master and develop branches, creating a new release.
- Hotfix branches: Created from the master branch to fix critical issues in the production code. Once the hotfix is complete, it is merged into both master and develop branches, ensuring the fix is applied to both the production and ongoing development codebases.

Git branching strategies like GitFlow provide a structured approach to development, enabling parallel work, isolating features, and maintaining a stable production codebase. 

</blockquote> 

</details>

---

51. What are Git hooks?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Git hooks are scripts that Git executes before or after specific actions, such as committing, pushing, or merging. They allow developers to automate tasks and enforce project-specific workflows.

Git hooks are customizable scripts that Git runs automatically in response to certain events during the version control process. They reside within the `.git/hooks` directory of a Git repository and can be written in any scripting language.

</blockquote> 

</details>

---

52. How do you squash multiple commits into a single commit in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To squash multiple commits into a single commit in Git:

- Use the interactive rebase command: `git rebase -i HEAD~n` (replace `n` with the number of commits to squash).
- In the interactive rebase file, change "pick" to "squash" (or "s") for the commits you want to squash.
- Save and close the file.
- Modify the commit message for the new squashed commit.
- Save and close the file.
- Git will perform the interactive rebase, squashing the specified commits into a single commit.
- If needed, force push the updated branch to the remote repository using `git push --force-with-lease`.

</blockquote> 

</details>

---

53. How do you use Git submodules?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To use Git submodules:

- Navigate to the root directory of your Git repository.
- Add a submodule by using the `git submodule add` command followed by the URL of the repository you want to add and the path where you want the submodule to reside.
- After adding the submodule, a new directory is created at the specified path. This directory represents the submodule and contains its own Git repository.
- Use `git submodule init` to initialize the submodule and fetch its contents.
- Use `git submodule update` to clone and checkout the latest commit of the submodule repository.
- Make changes within the submodule by navigating to its directory, making commits, and pushing changes to its repository as needed.
- In the main repository, commit and push the updated submodule reference to record the new submodule commit hash.
- To update the submodule to the latest commit in its repository, navigate to the submodule directory and use `git pull` or any other Git commands as needed.

Using Git submodules allows you to include and manage external repositories within your main repository, enabling separate versioning and development for the submodule. It is especially useful when you want to include external code as part of your project while maintaining the ability to update it independently.

</blockquote> 

</details>

---

54. Explain the difference between a fork and a clone in the context of GitHub. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Fork: A fork is a copy of a repository created by a user in their own GitHub account. It allows the user to freely make modifications to the repository without affecting the original project. Forking is commonly used for contributing to open-source projects, where users can make changes to their forked repository and propose those changes to be merged into the original repository via pull requests.

Clone: Cloning refers to creating a local copy of a repository from GitHub onto your own computer. Cloning allows you to have a complete copy of the repository, including all branches, commits, and files. It enables you to work on the code locally, make changes, and commit them to your local repository. Cloning is typically used when you want to work with the codebase locally, without the intention of contributing changes back to the original repository.

</blockquote> 

</details>

---

55.	How do you handle large files in a Git repository on GitHub?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To handle large files in a Git repository on GitHub, you can use Git's Large File Storage (LFS) extension.

- Install Git LFS: Download and install Git LFS on your local machine from the official Git LFS website.
- Initialize Git LFS: Navigate to your repository's root directory and run `git lfs install` to initialize Git LFS for your repository.
- Specify file types to track: Use `git lfs track` followed by file patterns or specific file names to specify which files should be tracked by Git LFS. 
- Add and commit changes: Add the large files to your repository as usual (`git add`, `git commit`). Git LFS will handle these files differently, storing their contents separately from the Git repository.
- Push changes to GitHub: Use `git push` to push your changes to the remote repository on GitHub. The large files will be uploaded to the Git LFS server, while the Git repository will contain pointers to these files.
- Share and clone the repository: Other users can clone the repository using `git clone`. Git LFS will automatically download the large files, replacing the pointers in the cloned repository with the actual file contents.

</blockquote> 

</details>

---

56.	What is the purpose of pull request reviews in GitHub, and how do you request and perform a review? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The purpose of pull request reviews in GitHub is to facilitate collaboration and ensure code quality by having peers review proposed changes before they are merged into a repository. Reviewers provide feedback, identify potential issues, and ensure that the code adheres to coding standards and best practices.
To request and perform a review in GitHub:

- Open a pull request: Create a pull request in the repository on GitHub, specifying the source and target branches for the proposed changes.
- Add reviewers: On the pull request page, add specific individuals or teams as reviewers. They will be notified and invited to review the changes.
- Reviewers perform the review: Reviewers examine the code changes, leave comments, and provide feedback on the pull request. They can review the changes in the "Files changed" tab, view discussions, and make inline comments.
- Address feedback: The author of the pull request responds to the feedback by making changes, replying to comments, and discussing any concerns raised by the reviewers.
- Iterative process: The author and reviewers may engage in multiple rounds of feedback and updates until the proposed changes meet the project's requirements and the reviewers' satisfaction.
- Approve the pull request: Once the reviewers are satisfied with the changes, they can approve the pull request. This indicates that they believe the changes are ready to be merged into the repository.
- Merge the pull request: Finally, the authorized person, usually a project maintainer or repository owner, merges the approved pull request into the target branch, incorporating the proposed changes into the codebase.

</blockquote> 

</details>

---
