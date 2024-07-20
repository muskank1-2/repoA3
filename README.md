# Scenario 1 : CONFLICT RESOLUTION 
According to the given scenario where I and My team mate are working on a proje ct on the same file and we made changes to the same line and commit them, now my team mate has merged the changes into the main branch and when I was trying to merge it too the main branch, a merge conflict occurred.

### Merge conflict
A merge conflict occurs when Git is unable to automatically resolve differences between two commits during a merge. This typically happens when two branches have made changes to the same lines in a file, or when one branch modifies a file that another branch deletes.

The merge conflict can only be solved mnaually using a text editor .

The steps I have taken to resolve merge conflict is shown below:-

1. Logged into my github accound and using the *new*  option in the top righ side of the github dekstop Created a git Repo named "repoa3"
![image](https://github.com/muskank1-2/repoA3/assets/169113658/a54d9bd2-2acb-4d83-b87c-c46330b7016a)



2. Now using windows powershell terminal I have cloned the git repo to the system using :

```bash 
 git clone https://github.com/muskank1-2/repoA3.git
```
After this, I created a file "project.txt" and added it and made the first commit using the following commands.
```bash
 echo "project.txt" >> project.txt
  git add project.txt
  git commit -m "first commit ft project.txt"
```

3. I pushed the file and changes to github using:
in the main branch
``` bash
git push origin main
```
The results of the step is shown in the ss here:
![image](https://github.com/muskank1-2/repoA3/assets/169113658/4db8c9da-69d8-4e54-8c30-e7bfdacf1f04)


4. Now in order to work with different branches I created a new branch names "b1" and "b2" using 
```bash
git branch <branch>
```
Now these branches have to be pushed to github thus after creating the branches I pushed them to github using 
```bash
git push origin <branch>
```
The results are shown here:
![image](https://github.com/muskank1-2/repoA3/assets/169113658/42e83549-27e7-4cde-a9f7-18dc56906636)


5. I checked out to branch "b1" in order to make changes and work with this branch using 
```bash
git checkout <branch>
```

6. I made the changes in the file within branch b1 as 
*"project.txt in branch b1"* and committed the changes.
These changes have to be pushed to Github and thus pushed the changes to github using the same command used before.

The results are shown as :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/d770cfeb-7fe9-4580-adcf-2032db089d51)


7. After this I did the same with branch b2 and made different changes in same line as *"project.txt in branch b2"* and pushed it to Github
The results are shown here:
![image](https://github.com/muskank1-2/repoA3/assets/169113658/46cd33ee-0df8-472a-bcdc-5347992ba941)


the github deskstop, with *repoa3* looks like this:
![image](https://github.com/muskank1-2/repoA3/assets/169113658/780d6f19-8500-4290-8dd5-7d93f75f0ece)


8. Now as changes have been made in the file from both the branches i.e. b1 by me and b2 by my teammate *(as per the scenario)*
I will checkout to main branch and merge **b1** in the **main** branch first and then push the changes to Github
And then we will merge **b2** !
At this step merge conflict occurs as shown :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/ccac85f2-2c71-4326-9d88-1c8594f7c1f7)



9. Now in order to let git accept the changes we will have to tell git which changes to accept among branch b1 and b2 and thus this will be done manually.
we see the conflict makers and thus we will remove the "<<<<<","=====" and ">>>>>" and will make the changes in the file.

we can also use echo command to resolve the conflict for small changes:

10. After making the changes we added the file and commit the changes in "project.txt"

![image](https://github.com/muskank1-2/repoA3/assets/169113658/edc6a558-cae2-4b91-88ed-6db665e75a10)


11. After all this we will check for the merge conflict status omce we have pushed the changes to github using 
```bash 
git status
```
![image](https://github.com/muskank1-2/repoA3/assets/169113658/2734b37f-9748-4041-8ad8-48b6b5fea6db)


12. further we will Review the commit *log* to ensure the merge commit is present and check its message to confirm it indicates the conflict was resolved:
 ![image](https://github.com/muskank1-2/repoA3/assets/169113658/23bd4155-aadc-4aa0-9f4f-7e4ef11a04ba)


Thus here the Merge conflcit has been resolved.

# senario 2 : Add Files and Commit Together
Task: I have worked on multiple files and want to add them and commit using a single command.

1. To do so we will first create the files for the same repo using terminal in notepad and the add all the files together using 
```bash
git add -A
```
After doing so we will commit the changes all at once using the *commit* option and then push the files to github  
2. We now will verify for the commit using 
```bash
git log
```

This command shows you the commit history, including the most recent commit at the top. Verify that your commit message appears in the log to confirm that the changes were committed as intended.

the results are shown as :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/45402888-6fda-43da-aa33-7574bd64bddc)


# scenario 3 : Include Additional Commit in the Previous Commit Message
Task : Task: You have just made a commit but realize you forgot to include a file and make a small typo correction. Instead of creating a new commit, you can amend the last commit to include these changes without altering the commit message. Also verify the amended commit by checking the commit

So, acc to the given scenario,
I have just made some changes in the files and then made a commit but now I want to change it and make some corrections and for that instead of making a new commt I will amend the original commit using the following command :
```bash 
git command -amend -m "message"
```

#### The results looks like this before amend 
![image](https://github.com/muskank1-2/repoA3/assets/169113658/a472b68f-3cea-4ee4-99e9-e2db7b760e25)

![image](https://github.com/muskank1-2/repoA3/assets/169113658/fe4ccfcf-8147-41a2-96b7-8e4b99cf867a)


As I have made the commit after adding the 4 files , *"updated content"* , I am changing it to "Added four files for scenario2 and amending for scenario3" using amend as shown :

![image](https://github.com/muskank1-2/repoA3/assets/169113658/fe089c3f-fc75-48e8-b6a0-7bf19eb57846)


# scenario 4 : Stash Command
At times when we dont want to commit our changes but save it, we can use stash command so that we can save your uncommitted changes temporarily and can switch tasks without committing those changes.

Here, I have made a file *filescenario4.txt* and stashed it with the following command 
```bash
git stash
```
checked the status of the file 
The results are shwon as :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/e1d26cef-3967-4bc8-b65c-5ff46bec0c04)

## other Stash commands 
  > git stash save "name" = temporarily stashes changes you have made to your working copy so you can work on something else,and then come back and re-apply them later on.
  > git stash apply = reverts the stash command
![image](https://github.com/muskank1-2/repoA3/assets/169113658/c4eb9afa-175d-44f2-8e65-fc361a0d8b0c)

   > git stash list = it will pull up a list of your repository stashes.
![image](https://github.com/muskank1-2/repoA3/assets/169113658/5e5a88b6-9a63-44c3-9541-38454b4402c9)

   > git stash pop = it removes or throws away the latest or the topmost stash.
   Here in the image I have used *git pop* and *git list* to show the changes made after delelting stash using pop, by the end we dont have any stash.
![image](https://github.com/muskank1-2/repoA3/assets/169113658/6b1dcde9-cee3-431b-a599-20d282bb3cbd)

# scenario 5 : Use of .gitignore
Task: You have files in your project that should not be tracked by Git, such as log files or build artifacts.

There are scenarios where we dont want some files to be tracked and thus keep them in un
save our uncommitted changes temporarily so you and switch tasks without committing those changes.

1. Now ro achieve this task I have initialised a git repositori name *gitig* and created two filed in it (tracked_file.txt, ignored_file.log).
```bash
echo "This file should be tracked" > tracked_file.txt
echo "This file should not be tracked" > ignored_file.log
```

2. staged the files and made the changes to commit.
(Only the *tracked_file.txt*)

```bash
git add tracked_file.txt
git commit -m "Added trackedfile"
```

3. After this I created a new file *.gitignore* and specified patterns for the files that should be ignored (here, *.log* for *ignore.log* file)
```bash
echo ".log" > .gitignore
```
4. I will then stage and commit the file using :
```bash
git add .gitignore
git commit -m "Excluding log files"
```

5. Now I will check the status and it will show the untracked file ,*ignore.log* 

The results are shown here :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/7e0d9536-43ab-4df3-a90e-b4fc45229cb6)


This occurred because the pattern specified with *.gitignore* doesn't match the pattern of that file and thus we can edit/add the patterns of the file which we dont want to track using any texteditor in the *.gitignore* file .

![image](https://github.com/muskank1-2/repoA3/assets/169113658/cb15f18c-0d2c-495f-940d-450ffb96d683)

After updating the pattern I will stag and commit the
changes made using 
```bash 
 git add .
 git commit -m "updated .gitignore"
```

6. Now check the status to verify and there will be a message "working tree clean" 


Results :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/1d00b6ba-7654-4439-9556-24b3a4a1e4f0)

Thus this shows the succes of .gitignore 

### Real-Life Use Cases of .gitignore
1. Excluding Logs and Temporary Files

During development and debugging, applications generate log files and temporary files that should not be tracked by Git.

2. Excluding Sensitive Information

In many projects, you might have configuration files that contain sensitive information such as API keys, passwords, and other credentials. These should not be committed to the repository and thus using .gitignore we can untrack them 

3.  Excluding Dependency Directories

Dependency directories managed by package managers often contain thousands of files that should not be committed to the repository. These can be easily regenerated by the package manager.

# scenario 6 : Revert Commit 
I have created a file *file_s6.txt* and made "first commit", then I have made another commit *commit to revert*
now I want to revert to my previous commit, to undo this mistake 

made the first commit for file **file_s6
using 
```bash 
git commit -m "message"
```
then made another commit after some changes in the file using the same commit command with different message as stated, Now I have to revert the commit for which I will user :
```bash
git revert <commit-hash>
```
 The <commit hash> can be obtained from the detailsof commit using : 
 ```bash
 git log 
 ```
 The results are as shown :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/3c01c345-5402-475f-9efc-dd9f88e4e072)

 The hash is copied from :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/8aa7a25b-f129-4937-ba1e-bc09ec5f7619)

After this the *revert* command is run and the commit is reverted

![image](https://github.com/muskank1-2/repoA3/assets/169113658/6b2c9809-e6f2-4461-accc-3ea0f403cd69)


I have done this and the results are as shwon :


![image](https://github.com/muskank1-2/repoA3/assets/169113658/11191377-1254-440a-9951-2326cea90499)

# Scenario 7 : Pull Request 
Task : You have made changes on a feature branch and want to merge them into the main branch via a pull request.

A pull request is a way to propose changes to a codebase/repository , discuss them and review them before we actually merge them inyo the main branch.

1. In order to achieve this task  I have to pull the latest changes made in the main branch using 
```bash
git checkout main
git pull origin main
```

2. Now I will create a new branch named *feature* and will switch to it using the following command :

```bash
git checkout -b feature-branch
```

3. After this Here, I created a file *"feature.txt"* and other 3 files which were already added, made the changes and added the content into it after which I added the changes and made a commit 
```bash

git add feature.txt
git commit -m "Added feature content"

```

4. Now all this changes has to be pushed to github repo and thus using push we I pushed the changes 
```bash
git push origin feature
```

![image](https://github.com/muskank1-2/repoA3/assets/169113658/8c9a1b01-4896-41a9-a0e6-eac96967156e)


5. This step actually involves creating the pull request and for which I created a pull request to merge the Feature branch into the **main** branch 

![image](https://github.com/muskank1-2/repoA3/assets/169113658/ee3f3762-e585-4146-8e81-0bde691e68aa)


For this I navigated to my github repository *"repoA3"*
and will click the *create pull request* prompt for the recently pushed branch *feature*.
After selecting the feature branch and the source and main branch as the base branch , I will pull the request.

![image](https://github.com/muskank1-2/repoA3/assets/169113658/c25508d1-bb9d-45a0-8565-a9aaddcf3fc2)


6. There is a description box where we have to add the description of our branch and the changes . So I wrote the description according to the features my file contains.
![alt text](image-26.png)

7. After this confirm the merge pull request and in this way a pull request is efficiently created.

The results are shown as :
![image](https://github.com/muskank1-2/repoA3/assets/169113658/de632cbc-6749-458b-9c76-92372f9a8367)

![image](https://github.com/muskank1-2/repoA3/assets/169113658/5ecd4a19-1467-4322-89bf-d3da0d969c12)


# ASSIGNMENT QUESTIONS 
### Why do we create branches in a repository and why do we create pull requests instead of merging directly?

Branches in a repository allow developers to work on features, fixes, or experiments in isolation from the main codebase. This prevents unstable code from affecting the main branch. 

Pull requests (PRs) enable code review and discussion before merging changes, ensuring code quality and allowing collaboration. They also provide a record of the proposed changes, reasoning, and the approval process, which is valuable for tracking and accountability.

### What is the difference between git add . and git add <filename>? What will we use when we have changes in multiples but we are not required to add some files?

*git add .* stages all changes in the current directory and subdirectories, while git add <filename> stages only the specified file. When you have changes in multiple files but do not want to add some, you can use git add <filename> for each specific file you wish to stage. Alternatively, you can use git add -p to interactively select hunks of changes to add.

### What is the difference between git fetch and git pull?

'git fetch' updates the local repository with changes from the remote repository but does not merge them into the local working branch. git pull combines git fetch and git merge, fetching changes from the remote repository and immediately merging them into the current branch. git fetch is safer for reviewing changes before merging, while git pull is convenient for automatic updates.

### What is a head in a repository and what does it do?

The HEAD in a Git repository is a pointer that indicates the currently checked-out branch or commit. It represents the current working state and the branch where new commits will be made. By switching HEAD, you can change the active branch or move to a different commit, facilitating branch management and version control.

### What is the .git folder in a repository?

The .git folder is a hidden directory at the root of a Git repository that contains all the metadata and object database for the version control system. It stores information about the repository's history, branches, tags, configuration, and the actual commits. This folder is crucial for Git's operation, enabling all version control functionalities.

### What are commit hashes and its use cases?

Commit hashes are unique identifiers (SHA-1) for each commit in Git. They ensure integrity and traceability by uniquely referencing specific commits. Use cases include pinpointing exact changes, reverting to previous states, referencing commits in commands (e.g., git checkout <hash>), and collaborating by sharing commit references.

### Different ways of syncing a branch with origin.


1. 
>> Fetch: Update your local repository with the latest changes from the remote without merging them into your current branch.
```bash
git fetch origin
```
>> Merge: Merge the fetched changes into your current branch. This creates a merge commit.
```bash
git merge origin/<branch-name>
```
or
```bash
git pull origin <branch-name>
```
>> Rebase: Alternatively, you can rebase your local changes onto the updated remote branch. This keeps a cleaner commit history by moving your changes to the tip of the updated branch.
```bash
git rebase origin/<branch-name>
```

2. Combine the fetch and rebase steps into a single command, pulling in the remote changes and rebasing your commits on top.
```bash
git pull --rebase origin <branch-name>
```
3. Push Forcefully:

In rare cases where you need to overwrite remote changes with your local changes (not recommended unless you understand the implications and have communicated with your team), you can force push:
```bash
git push --force origin <branch-name>
```
or safer alternative:
```bash
git push --force-with-lease origin <branch-name>
```
All these steps can be used to sync a branch with origin.


# Extra Learnings 
1. #### git reflog - this helps to display a history of all changes to the current files branches HEAD refrence and this helps to recover from mistakes and understand the repository' state , while git log is used to display the commit history of the current branch and shows a list of commits, along with details like commit hash, author, date and commit message.
2.  ### git cat <file name> - this helps in checking the contents of a particular file we have created
3.  ### git cherry-pick - this helps to make changes introduced by an existing commit onto the current branch< this is helpful when we want to aplly specific chages from one branch to another without merging the entire branch.

   git cherry-pick <hash of the commit>
   
