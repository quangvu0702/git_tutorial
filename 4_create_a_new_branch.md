# Create a new branch
  - Why do we need many brands?
  - Create new brand.
  - Checkout to new brand.
  - Create new files, and modify new file.
  - Commit to local git.
  - Push new brand to server git.

1. Why we nead many brands.
   - Do you remember the command we use when we push "local git" to "git server"
   ```
   git push origin master
   ```
   - "master" is a branch. We can create as many as posible branch. But why we need many branch. 
   - I will give you 2 cases that show creating more branch is better than using only branch "master".
     - Case 1 - Story of a developer. I will tell you a story about David:  
     David love develop feature. He is a developer. David usually try his ideas on his machine it is a desktop. 
     At the end of day, he pushes code to the branch named "feature_101" to save the work and go home.
     After dinner, he have want to keep working, then he pull code from the branch "feature_101" and keep working.
     For a week working very hard, David have finished his ideas. He push all code to branch "feature_101" then create a ***pull request*** to branch "master".
     David will wait his colaborator review his code style, policies, ... 
     After pass on review David's code on "feature_101" will be merge to "master" and deployed to production.
     - Case 2 - Story of Harry, Ron, and Hermione: Professor Snape gives an coding assigment to the group Harry, Ron, and Hermione.
     There are 3 exercises in the assigment. Harry chooses exercise 1, Ron chooses exercise 2, and Hermione do exercise 3. 
     So they create a repository name "Assigment". Then Harry create a branch "exercise_1", Ron create a branch "exercise_2", 
     and Hermione create a branch "exercise_3". After that they create pull requests to "master". 
     Code in branch "master" is final code they want to summit.
     
   - (Note) When deploy a product we using code on a branch - the default is branch "master".
     And technical team assumption that code in branch "master" is runable anytime on production. 
     So we need other branchs to contains the code that is developing. The code flow will be "any branch" > "master".
     
2 Create new brand:
  - To create a branch we using command "git checkout -b [name_of_your_new_branch]". 
  For example in repo "hello-world" we want create a branch "hello-adele"
  ```
  git checkout -b hello-adele
  ```
  - The out screen will be: "Switched to a new branch 'hello-adele'" 
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/create_branch.png "create branch")
  
  - This means branch "hello-adele" and we are in branch "hello-adele". 
  - we can work here, modify files, delete file, add file but these actions do not effect to branch "master" and others brands.
  - Now we can feel the benefit of create new branch.
  - Let check status:
  ```
  git status
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_9.png "git status 9")
  - Status show that "On branch hello-adele".
  - Let list all branch:
  ```
  git branch
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_branch.png "git branch")
  - We can see that we have 2 branch: master and hello-adele.
3. Checkout to new brand.
  - Let go back to branch master:
  ```
  git checkout master
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_checkout.png "git checkout")
  - We are "Switched to branch 'master'".
  - Let come back to branch 
  ```
  git checkout hello-adele
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_checkout_2.png "git checkout")
  
4. Create new files, and modify new file:
   - Create new files and modify the file. 
   In this case I will create new file "hello.txt" and put lyric of this song to that file.
   - Let check status: <br />
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_10.png "git status")
   - This is new file. We will "add" to index file, "commit" to put indexed files to "local git", and "push" to push "local git" to "git server".
5. Commit to local git:
   - Index file 'hello.txt'
   ```
   git add hello.txt
   ```
   - Commit to local git:
   ```
   git commit -m 'add hello.txt to new branch'
6. Push new brand to server git.
   ```
   - Push to git server:
   ```
   git push origin hello-adele
   ```
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/whole_process.png "git whole process")
   
   - Now we know how to create new branch. 
   - Let see what we have on git server: Yay we have a new branch. <br />
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_5.png "git whole server 5")
  
