# First_commit:
  - Create new files.
  - Create new folders.
  - Add new files and folders.
  - Commit new files and folders to local git.
  - Push your files and folders to server git.
  - Example: https://github.com/quangvu0702/hello-world
  
After we clone the repository named "hello-world", we will have folder "hello-world" in our computer. Go inside the folder "hello-world".
```
cd hello-world
```
1. Create new files:
   - In the previous session 1_introduction.md, we have created a git repository named "hello-world" and cloned it to local git.
   - Now we have folder "hello-world" in local git. Create a file named "README.md" in folder "hello-world"
   - Add new line "The first file will be commit.' into the file "README.md"
   - Use command "git status" to check the status of git.
  ```
  git status
  ```
  - The output screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_example.png "repo-name")
  
2. Create new folders:
   - Create folder "files" and folder "images" in folder "hello-world".
   - Use command "git status" to check the status of git.
  ```
  git status
  ```
  - The output screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_example.png "git status")
  - The status does not show the two new folders "files", "images". The reason is that git cannot detect the empty folders.
  - The trick is that you can add any file into the folder to make it not empty. 
  In this case we will create the file ".keep" in both folders "files" and "images".
  - Let check the status of git now: 
  ```
  git status
  ```
  - The output screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_2.png "git status 2")
  
  - Now git can see two folders: "files" and "images".
  
3. Add new files and folders to the index:
  - We have three new definition: "local file", "local git", and "server git".
    - "local file": all files in the folders.
    - "local git": the git on our local machine that has some relationship with server git.
    - "server git": the git that you can access from the web. Example: https://github.com/quangvu0702/hello-world
    <br />
    Don't be panic. We will make this clear through the examples below:
  - Remember we have in our computer the folder "hello-world" containing: <br />
    - README.md 
    - files/.keep
    - images/.keeps
    This is what we call "local file".
  - We have to index files before moving files from "local file" to "local git". In the folder "hello-world" we have 3 files: "README.md", 
  "files/.keep", "images/.keep". We just want to index one file "README.md" to "local git".
  ```
  git add README.md
  ```
  - Let check the status now: 
  ```
  git status
  ```
  - The output screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_3.png "git status 3")
  - The file "README.md" have been indexed and tracked by git. We can see two untracked files: "files/" and "images/".
  This means all files in folders "files/" and "images/" are untracked. 
  This signifies that "local git" doesn't know anything about these files regarding both the content and status.
  - We need to commit new files and folders to local git: After indexing files, we copy the indexed files to the "local repo" or "local git".
  ```
  git commit -m "This is a basic commit message."
  ```
  - Let check the status now: 
  ```
  git status
  ```
  - The output screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_4.png "git status 4")
  
4. Push our files and folders to server git
  - Now our "local git" has file "README.md". Let's go to web and check our repo on "git server". 
  For example my git repo is: https://github.com/quangvu0702/hello-world
  My screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server.png "git server 4")
  - We can see that our "hello-world" is empty. There is no file "README.md". 
  Because we have justed commited the file "hello-world" to "local git".
  We did not push "local git" to "server git" yet.
  - Now we push "local git" to "server git": we will be asked for username and password)
  ```
  git push origin master
  ```
  - Now our "local git" have been pushed to "server git". Let's go to web and check our repo on "server git" again. 
  For example my git repo is: https://github.com/quangvu0702/hello-world
  My screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_2.png "git server 2")
  - Now we can see file "README.md" in our repository.
  - Yay!!! We have created a file, committed it to "local git" and pushed it to "server git".
