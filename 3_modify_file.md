# Modify_file:
  - Modify a file.
  - Commit the modified file to local git.
  - Push the committed file to server git.

1. Modify a file: 
   - Open "README.md" and add a new line to the file :"The second line wil be commited.".
   - Check the status of git.
   ```
   git status
   ```
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_5.png "git status 5")
   
2. Commit the modified file to local git.
    - Add "README.md".
    ```
    git add README.md
    ```
    - Check the status.
    ```
    git status
    ```
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_6.png "git status 6")
   
    - Commit to "local git"
    ```
    git commit -m 'Commit modified file README.md'
    ```
    - Check the status.
    ```
    git status
    ```
    
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_7.png "git status 7")
    - We see "Your branch is ahead of 'origin/master' by 1 commit." on the screen. 
    This means that "local git" has one commit that don't exist on " server git".
    - The new commit is not pushed to "server git" yet.
    - Let's go to git website and check the repostitory "hello-world". My repo is: https://github.com/quangvu0702/hello-world.
    
    ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_3.png "git server 3")
 3. Push the committed file on "local git" to "server git".
    ```
    git push original master
    ```
    - Let check the status again:
    ```
    git status
    ```
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_8.png "git status 8")
   - We can see that "Your branch is up-to-date with 'origin/master'". Now "local git" is in the same status with "server git".
   - Let's go to git website and check the repostitory "hello-world" again.
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_4.png "git server 4")
   - Warning: because our file "README.md" is in format md, we cannot see the new line. 
   But we will see "The first file will be commit. The second line wil be commited." in the same line. It is ok. Don't worry.
   
   - Now we can create new repository, add files, modify files, commit files to "local git" and push files to "server git". In the next session we will learn to create a branch, and get to know why we need to create new branch.
   
 4. Your exercise now is to create new files, then commit them to "local git" then push to "server git".
    - Hint: 
    ```
    git add
    git commit 
    git push original master
    ```
