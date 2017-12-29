# Create a new branch
  - Why do we need many branches?
  - Create a new branch.
  - Checkout to the new branch.
  - Create new files, and modify new files.
  - Commit to local git.
  - Push the new branch to server git.

1. Why do we need many branches?
   - Do you remember the command we use when we push "local git" to "server git"
   ```
   git push origin master
   ```
   - "master" is a branch. We can create as many branches as posible. But why?
   - I will give you two cases that can show creating branches is better than using only one branch "master".
     - Case 1 - Story of a developer. The below story is about David:  
     David is a developer. He loves develop features. He usually tries his ideas on his machine, which is a desktop. 
     At the end of day, he pushes the code to the branch named "feature_101" on server git to save the work and goes home.
     After having dinner, he wants to keep working, so he pulls the code from the branch "feature_101" and then he can keep working.
     After a very hard-working week, David has finished his ideas. He pushes all the codes to his branch "feature_101" on server git and 
     then creates a ***pull request*** to his branch "master", which is a workspace of David and his collaborator. After the pull request, 
     David will wait for his colaborator to review the code style, code policies... 
     After passing the review, David's code on the branch "feature_101" will be merged to branch "master" and deployed to production.

     - Case 2 - Story of Harry, Ron, and Hermione: Professor Snape gives an coding assignment to the group Harry, Ron, and Hermione.
     There are three exercises in the assignment. Harry chooses exercise 1, Ron chooses exercise 2, and Hermione will do exercise 3. 
     So they create a repository named "Assignment". Then Harry creates a branch "exercise_1", Ron creates a branch "exercise_2", 
     and Hermione creates a branch "exercise_3". After finishing the exercises, they create pull requests to the branch "master". 
     The code in branch "master" is the final code that they want to summit.
     
   - (Note) When deploying a product we normally use code in a branch - the default is branch "master".
     Technical team often assume that code in branch "master" is runable at anytime on production. 
     So we need other branches for the code that is in developing stage. The code flow will be "any branch" > "master".
     
2 Create a  new branch:
  - To create a branch we using command "git checkout -b [name_of_your_new_branch]". 
  For example in repo "hello-world" we want to create a branch "hello-adele"
  ```
  git checkout -b hello-adele
  ```
  - The output screen will be: "Switched to a new branch 'hello-adele'" 
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/create_branch.png "create branch")
  
  - This means that we are in branch "hello-adele". 
  - we can work here, modify files, delete files and add files but these actions do not effect the branch "master" and others branches.
  - Now we can see the benefits of creating new branches.
  - Let's check the status of git:
  ```
  git status
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_9.png "git status 9")
  - The output screen shows that "On branch hello-adele".
  - Let's list all branches:
  ```
  git branch
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_branch.png "git branch")
  - We can see that we have two branches: master and hello-adele.
3. Checkout to the new branch.
  - Let's go back to branch "master":
  ```
  git checkout master
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_checkout.png "git checkout")
  - We are "Switched to branch 'master'".
  - Let's come back to branch "hello-adele"
  ```
  git checkout hello-adele
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_checkout_2.png "git checkout")
  
4. Create new files and modify new files:
   - Create new files and modify the files. 
   In this case I will create new file "hello.txt" and put the lyric of this song to that file.
   - Let's check the status: <br />
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_10.png "git status")
   - This is new file. We will "add" to index file, "commit" to put indexed file to "local git", and "push" to push "local git" to "server git".
5. Commit to local git:
   - Index file 'hello.txt'
   ```
   git add hello.txt
   ```
   - Commit to local git:
   ```
   git commit -m 'add hello.txt to new branch'
   ```
6. Push new branch to server git.
   
   - Push to git server:
   ```
   git push origin hello-adele
   ```
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/whole_process.png "git process")
   
   - Now we know how to create a new branch. 
   - Let's see what we have on server git. Yay we have a new branch. <br />
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_5.png "images")
  
