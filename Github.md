- [ ] **Why do we use github/git?**
 - It lets you and others work together on projects from anywhere by storing remote copies 
  of your projects/repositories (github servers) as backup of your local copies.
  
- [ ] **What happens when you clone a repository?**
  
 When you clone a repository, it creates a local copy on your computer and sync between the two locations.

  _IN DETAILS_

 1- point to an existing repo and make a clone or copy of that repo in a new directory, at another location. 

 2- cloning automatically creates a remote connection called "origin" pointing back to the original repository.

 *"This makes it very easy to interact with a central repository."*

- [ ] **What happens when you fork a repository?**

  - An exact replica of the repository is created on your individual user account.
  
   - **The main point of forking**
  >   A fork is a copy of a repository that allows you to freely experiment with changes without affecting the original        project.
 Forks act as a sort of bridge between the original repository and your personal copy. You can submit Pull Requests to help 
 make other people’s projects better by offering your changes up to the original project. 
 *"Forking is at the core of social coding at GitHub."*
 
   - **Forks differs from clone in..**
  >      A forked repository differs from a clone in that a connection exists between your fork and the original repository
  itself. In this way, your fork acts as a bridge between the original repository and your personal copy where you
  can contribute back to the original project using Pull Requests.
  
  - [ ] **What happens when we do git pull origin master**
  git pull origin master pulls the master branch from the remote called origin into your current branch.
  
  - [ ] **How do we create a new branch on our local machine?**
  
  ``` git checkout branchName ```
  
  - [ ] **When we make a change to a file, how do we tell git to track it?**
  
  ``` git add fileName ```
  
  - [ ] **When we have finished working on a branch, how do we make sure that our changes do 
  not cause a conflict with master? (this can all be done locally)**
  
  ``` git checkout master
      git pull origin master
      git checkout myBranch ```
      *merge the master into your branch and solve conflicts*
      
      - [ ] **What does git push origin [branch-name] do?**
      
      makes your local branch on remote
      
      - [ ] **Why do we make pull requests instead of just changing master directly?**
      
      so all team members can review the changes and agree on them.
      enables easy peer-review of the code. Instead of pushing directly through to master, 
      everyone can comment on the changes and ask questions before merging any piece of work. /// more
      
      - [ ] **Why is it important to run our team member’s branches when they make a pull request?**
      
      - [ ] **This is the working process you should follow, try to explain what happens at each step/why we do it:
git clone [repository]
git checkout -b new-feature
make some changes to index.js
git add index.js
git commit -m "added a cool new feature"
since we started, our partner has merged another branch into master
git checkout master
git pull origin master
git checkout new-feature
git merge master
merge conflict happens in index.js we fix it
git add index.js
git commit -m "fix merge conflict"
git push origin new-feature**
  
  // later
  
