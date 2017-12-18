# Modify_file:
  - Modify a file.
  - Commit modified file to local git.
  - Push the committed file to server git.

1. Modify a file: 
   - Open "README.md" and add new line "The second line wil be commited.".
   - Check status.
   ```
   git status
   ```
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_5.png "git status 5")
   
2. Commit modified file to local git.
    - Add "README.md".
    ```
    git add README.md
    ```
    - Check status.
    ```
    git status
    ```
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_6.png "git status 6")
   
    - Commit to "local git"
    ```
    git commit -m 'Commit modified file README.md'
    ```
    - Check status.
    ```
    git status
    ```
    
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_7.png "git status 7")
    - We see that "Your branch is ahead of 'origin/master' by 1 commit." on the screen. 
    This means "local git" have one commit that don't exist in "git server".
    - New commit is not pushed to "git server" yet.
    - Let go to git web-site and check repostitory "hello-world". My repo is: https://github.com/quangvu0702/hello-world.
    
    ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_3.png "git server 3")
 3. Push "git local" to "git server".
    ```
    git push original master
    ```
    - Let check status again:
    ```
    git status
    ```
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_8.png "git status 8")
   - We can see that "Your branch is up-to-date with 'origin/master'". Now "local git" is the same with "git server".
   - Let go to git web-site and check repostitory "hello-world" again.
   
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_4.png "git server 4")
   - Warning: because our file "README.md" is in format md. We cannot see the new line. 
   But we will see "The first file will be commit. The second line wil be commited." in the same line. It is ok. Don't worry.
 4. Your exercise is create new files, then commit to "local git" then push to "git server.
    - Hint: 
    ```
    git add
    git commit 
    git push original master
    ```
