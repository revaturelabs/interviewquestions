## Technical

1. What is `Git`?

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is a very famous tool which facilitates source code management in software development.
- We can track changes in computer files (versions) using `Git`.
- Using git can track the progress of a project over time as well as coordinate work among team developers.
</blockquote> 

</details>

---
2. What is the difference between `Git` and `GitHub`?

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is a version control tool, used to manage the history of changes performed to source code.
- Whereas `GitHub` is a web application that provides service to host source code, commonly referred to as Git repository.
- `GitHub` provides all of the distributed version control and `source code management (SCM)` functionalities of Git, along with a few of its features.
  
</blockquote> 
    
</details>

---
3. What do you understand by Git repository?

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Git repository refers to a folder/location where all the Git files are stored.
- These files can either be stored on the local repository or the remote repository.
- The local repository is the folder inside your system where you will find one hidden folder named `.git` 

</blockquote> 

</details>

---

4. What do you mean by initializing a repository in Git? How do we do it?

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

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Ideally, the contents of the  .git folder are modified by the `git` command, we are not supposed to tamper with any files manually.
- The .git folder contains all information that is necessary for the project and all information relating to commits, remote repository address, etc. 
- It also contains a log that stores the commit history and helps to roll back to the desired version of the code.
</blockquote> 

</details>

---

6. How to view commit logs in git?

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

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The project files that we are currently working on are called working trees,or working directory
- We can think of a working tree as a file system where you can view and modify files.
  
</blockquote> 

</details>

---

8. What is the staging area in Git?

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The staging area also called an index, is where commits are prepared. 
- The index compares the files in the working tree to the files in the repo. 
- When you make a change in the working tree, the index marks the file as modified before it is committed.
  
</blockquote> 

</details>

---

9. How to copy the remote repository onto your local machine?

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

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Untracked files are files that have been created within your repo's working directory but have not yet been added to the repository's tracking index using the `git add command.
  
</blockquote> 

</details>

---

15. What is a source code repository?

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

A source-code repository is an archive with the code as well as the hosting facility for these software archives, where you can also have the project’s technical documentation, web pages, snippets, patches, etc. which can be accessed publicly (open-source) or privately.

</blockquote>

</details>

---

16.  What are the benefits of the source code repository?

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

18. how do you solve merge  conflict?

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

19. give some git  commands?

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

23. How do you request a merge request with GitHub?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To request a merge request with GitHub, follow these steps:

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

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

There are many patterns that can be followed for Git management, but one common pattern is the Gitflow workflow. In this pattern, development is done in feature branches that are merged into a develop branch. Releases are made from the develop branch, and hotfixes are done in separate branches that are merged into both the develop and master branches. The master branch always represents the latest production release.

</blockquote> 

</details>

---

26. What are the steps to setting up a Git repo?

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

27. What repositories do you know?

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

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To avoid overwriting each other's changes when working on the same file in Git, you can use branches. Each person can work on a separate branch and then merge their changes into the main branch when they're ready. Alternatively, you can use a pull request workflow, where one person submits their changes as a pull request and the other person reviews and approves the changes before merging them into the main branch.

If you both need to work on the same file simultaneously, you can use a version control system that supports locking, where only one person can make changes to the file at a time. However, this can be less efficient and more prone to conflicts than using branches or pull requests.

</blockquote> 

</details>

---

30. What is git flow, work flow? 

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

- Git flow is a branching model used in Git. 
- It is used to define a strict branching model designed around the project release. 
- Git flow consists of various branches, such as feature, release, and hotfix branches, to help manage the development process. 
- A typical Git flow workflow involves creating a feature branch from the develop branch, making changes to the feature branch, merging the feature branch back to the develop branch after testing, creating a release branch, and then merging the release branch into the master branch after testing.

 </blockquote> 

</details>

---

31.  What version control did you use for your team projects?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
We used Git as the version control system for our team projects. Git is a popular distributed version control system that allows multiple developers to work on a project at the same time and track changes made to the codebase. It provides various features like branching, merging, and staging, which make it easy to manage code changes and collaborate effectively with team members. 

</blockquote> 

</details>

---

32.  explain Git and version control and how you used it in training 

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Git is a distributed version control system that allows developers to track changes made to the codebase and collaborate effectively with team members. It provides various features like branching, merging, and staging, which make it easy to manage code changes and collaborate effectively with team members. Git allows developers to work on a project locally and then push changes to a remote repository, which can be accessed by other team members.

In training, we used Git to manage the code changes made during the development process. We used Git to create branches, make changes to the code, and merge changes back into the main branch after testing. This allowed us to keep track of code changes and collaborate effectively with team members. 

</blockquote> 

</details>

---

33. what was the hardest part of git keeping ?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
The hardest part of Git keeping is resolving conflicts that arise when two or more team members make changes to the same file. Git provides various tools and features to help manage conflicts, such as merging, rebasing, and pull requests. However, conflicts can still occur, especially in large codebases with many contributors. Resolving conflicts requires careful attention to detail and good communication between team members. 
    
</blockquote> 

</details>

---
34.  what was the hardest part of git keeping ?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The hardest part of Git keeping is resolving conflicts that arise when two or more team members make changes to the same file. Git provides various tools and features to help manage conflicts, such as merging, rebasing, and pull requests. However, conflicts can still occur, especially in large codebases with many contributors. Resolving conflicts requires careful attention to detail and good communication between team members. 
    
</blockquote> 

</details>

---

35. What's the most important things to consider when merging a pull request?

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

36. Explain the difference between the Github master/head and development branches.

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Git, the "master" branch is the default branch that contains the stable, production-ready code. The "head" branch refers to the most recent commit in a branch. The "development" branch, on the other hand, is a branch used for ongoing development work. It may contain code changes that are not yet ready for production, such as new features or bug fixes that are still being tested. The development branch is usually merged into the master branch once all changes have been tested and approved for production. 
    
</blockquote> 

</details>

---

37. If code does get overridden how would you go about fixing that?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

If code gets overridden in Git, there are several ways to fix it depending on the situation. 

One way is to use Git's "reflog" feature to find the commit that contained the original code and then revert the code back to that commit. 

Another way is to use Git's "rebase" command to rewrite the history of a branch and incorporate the original code changes into the current codebase. 

If the code was overwritten by mistake and the original code is lost, it may be possible to retrieve the code from a backup or from another team member who has a copy of the code. 
    
</blockquote> 

</details>

---

38. Did you pull request on GitHub?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Yes, I have used pull requests on GitHub for various projects. A pull request is a way to propose changes to a project's codebase and merge those changes into the main branch. Pull requests allow team members to review and discuss changes before they are merged into the main branch, which helps ensure that code changes are high quality and do not break existing functionality. 

</blockquote> 

</details>

---

39. Did you use Trello and Git for organization?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Yes, I have used Trello and Git together for project organization. Trello is a project management tool that helps teams organize tasks and track progress. Git is a version control system that allows developers to track changes made to the codebase and collaborate effectively with team members. We used Trello to track project tasks and used Git to manage code changes and collaboration with team members. 
    
</blockquote> 

</details>

---

40. "Did you have any difficulties with so many people working on a project or with Git?"

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Yes, working with a large number of people on a project can be challenging, especially when using Git. One of the main challenges is managing conflicts that arise when multiple team members make changes to the same file. Another challenge is coordinating the development process and ensuring that all team members are on the same page. However, Git provides various features and tools to help manage these issues, such as branching, merging, and pull requests. Effective communication and coordination between team members are also crucial for successful collaboration. 

</blockquote> 

</details>

---

41. What are the advantages and disadvantages of Version Control?

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

43. They use gera for now but are moving to start using GitHub.

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Moving from Gera to GitHub can be a good decision, as GitHub is a more popular and feature-rich platform for software development. GitHub provides many features that Gera may not offer, such as pull requests, code reviews, and continuous integration. GitHub also has a larger community of developers and users, which can make it easier to find help and collaborate with others. However, migrating to a new platform can also be challenging and require some adjustment. 

</blockquote> 

</details>

---

44. What is Git? Do you use GUI or CLI?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Git is a popular distributed version control system that allows multiple developers to work on a project at the same time and track changes made to the codebase. It provides various features like branching, merging, and staging, which make it easy to manage code changes and collaborate effectively with team members.

</blockquote> 

</details>

---

45. What is rebasing in Git?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 
Rebasing in Git is a process where a developer moves the changes made in one branch to a different branch. The developer essentially applies the changes made in one branch on top of the other branch. This can be useful in scenarios where there are changes in one branch that the developer wants to include in another branch. Rebasing helps keep the commit history linear and clean, which can make it easier to understand the development process. 

</blockquote> 

</details>

---

46. What is the difference between SVN repository and Git repository?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

The main difference between SVN (Subversion) and Git is that SVN is a centralized version control system, while Git is a distributed version control system. In SVN, all team members access a central repository, and changes made by each team member are merged back into this central repository. In Git, every team member has a local copy of the repository, and changes are synced between team members through pushing and pulling changes from a remote repository.

Another difference is that SVN tracks changes to individual files, while Git tracks changes to the entire codebase. Git provides better branching and merging capabilities than SVN, which makes it easier to manage code changes and collaborate effectively with team members. 

</blockquote> 

</details>

---
