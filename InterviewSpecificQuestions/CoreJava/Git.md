## Technical

1. What is `Git`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is very famous tool which facilitates source code management in software development.
- We can track changes in computer files (versions) using `Git`.
- Using git can track progress of project overtime as well as coordinate work among team developers.
</blockquote> 

</details>

---
2. What is difference between `Git` and `GitHub`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Git` is a version control tool, used to manage history of changes performed to source code.
- Whereas `GitHub` is a web application which provides service to host source code, commonly referred to as Git repository.
- `GitHub` provides all of the distributed version control and `source code management (SCM)` functionalities of Git, along with few of its own features.
  
</blockquote> 
    
</details>

---
3. What do you understand by Git repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Git repository refers to a folder/location where all the Git files are stored.
- These files can either be stored on the local repository or on the remote repository.
- The local repository is the folder inside your system where you will find one hidden folder named `.git` 

</blockquote> 

</details>

---

4. What do you mean by initialize a repository in Git? How we do it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Usually when the new project is created, developers first initialize the local repository using `Git` on their system.
- Initialize a repository in Git means creating a directory which will start tracking the changes to your files or source code.
- To do this, we first create a simple empty directory for our application and execute below command using Git-

```
git init
```

- After above command, a hidden `.git` folder will appear in the directory.
</blockquote> 

</details>

---

5. Can we modify `.git` hidden folder under any Git repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Ideally the contents of .git folder are modified by `git` command, we are not supposed to tamper any files manually.
- The .git folder contains all information that is necessary for the project and all information relating commits, remote repository address, etc. 
- It also contains a log which stores the commit history and helps to roll back to the desired version of the code.
</blockquote> 

</details>

---

6. How to view commit logs in git?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Git repository holds all of the commits (snapshot of all your files at a point in time) that have been made. 
- We can access the commit history with the below command.

```
git log
```

</blockquote> 

</details>

---

7. What is working directory/tree in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The project files that we are currently working on are called as working tree, or working directory
- We can think of a working tree as a file system where you can view and modify files.
  
</blockquote> 

</details>

---

8. What is staging area in Git?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The staging area also called as index, is where commits are prepared. 
- The index compares the files in the working tree to the files in the repo. 
- When you make a change in the working tree, the index marks the file as modified before it is committed.
  
</blockquote> 

</details>

---

9. How to copy remote repository onto your local machine?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- We can copy a remote repository onto your local machine using below command

```
git clone '<remote-repository-url>'
```

-  Above command will automatically set up a local master/main branch that tracks the remote master/main branch it was cloned from.
</blockquote> 

</details>

---

10. How to clone specifc branch using `git clone` command?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- To clone lets say feature branch named `feature/audit` from the GitHub remote repository we can use below command-

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

12. What is Git command to save your changes to the local repository?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `git commit` command is used to save your changes to the local repository.
- We need to ensure that we use the `git add` command to mark the desired changes for inclusion. 

```
git commit -m "Added first commit"
```

-  In above command we specifiy the message for the commit.

</blockquote> 
</details>

---

13. What is use of `git push` command?

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
    
- Untracked files are files that have been created within your repo's working directory but have not yet been added to the repository's tracking index using the `git add` command.
  
</blockquote> 

</details>

---

15. What is source code repository?

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
- **Version Control:** When developers make enough changes to a program stored in a source code repository, they can designate the updated program as a new “version” of the software. A repository also stores previous versions of a program, a feature which allows companies to restore a previous version if, for example, an update introduces a harmful bug.

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
