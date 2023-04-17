1. How would you resolve a merge conflict?

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

2. What is  Git and versioning?

<details><b>Show Answer</b></summary>

<blockquote>

**GIT**: It is a free and open-source distributed version control system. It is used to handle small to large projects with speed and efficiency.

**Versinioning**: Every codebase changes over a period of time and versioning is nothing but different copies of codebase over a period.

</blockquote>

</details>

3. What is version control?

<details><b>Show Answer</b></summary>

<blockquote>

**Version Control:** Version control is a system that records multiple versions(changes) of codebase or set of files over a period of time.

</blockquote>

</details>

4. Can you mention some git commands that you use very often?

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

5. How do you create your branch?

<details><b>Show Answer</b></summary>

<blockquote>

A branch is used to work on different versions of repository at same time.

- After the first commit the main branch is created.

Methods to create a new branch:

```git 
git branch <branch name>
git branch <branch name> <from branch>
```
</blockquote>

</details>

6. What commands do you use to update codes?

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

7. Tell about GitHub and its some features?

<details><b>Show Answer</b></summary>

<blockquote>

GitHub is a web-based platform that allows developers to store and manage their code, collaborate with others, and keep track of changes to their code using version control. Some of its features include repository hosting, issue tracking, collaboration tools, and integration with other software development tools.


</blockquote>

</details>

8. How do you distribute GitHub responsabilities on a organization?

<details><b>Show Answer</b></summary>

<blockquote>

Responsibilities for GitHub in an organization can be distributed based on factors such as repository ownership, issue tracking, collaboration, security and compliance, and training and support. The specific distribution of responsibilities will depend on the organization's size, structure, goals, and individual team members' skillsets.

</blockquote>

</details>

9.  What is the code repository?

<details><b>Show Answer</b></summary>

<blockquote>

- It is a centralized location where developers store and maintain and track the different versions of the codebase.

</blockquote>

</details>

10. What is a branch?

<details><b>Show Answer</b></summary>

<blockquote>

A branch is used to work on different versions of repository at same time.

- In git the first branch is `main` or `master`. From `main` branch multiple branhces can be created. A branch can also be created from any other existing branch of a git repository.



</blockquote>

</details>

11. Git vs GitHub?

<details><b>Show Answer</b></summary>

<blockquote>

- Git is a version control system used to manage changes to code, while GitHub is a web-based platform that provides hosting for Git repositories and additional collaboration features. 
- Git is a command-line tool used locally on a developer's computer, while GitHub is a web-based interface for managing Git repositories.

</blockquote>

</details>

12. On git, how do you see the changes you added to your code?

<details><b>Show Answer</b></summary>

To see the changes you've made to your code in Git, you can use the `git diff` command. This command will show the difference between the current state of the code and the previous commit.

To see the changes you've made in a specific file, you can use the command

```git
git diff <filename>
``` 

This will show the changes you've made to the file since the last commit.

If you've already added your changes to the staging area using git add, you can use the below command to see the changes that have been staged but not yet committed.

```git
git diff --staged
``` 

- You can also use a graphical user interface (GUI) tool such as GitKraken or Sourcetree, which can provide a visual representation of the changes you've made to your code.

<blockquote>



</blockquote>

</details>