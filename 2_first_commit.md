# First_commit:
  - Create new files.
  - Create new folders.
  - Add new files and folders.
  - Commit new files and folders to you local git.
  - Push your files and folder to server git.
  - Example at: https://github.com/quangvu0702/hello-world
1. Create new files:
   - In the previous 1_introduction.md we have create a git repository "hello-world" and clone it to local.
   - Now we have folder "hello-world" in you local. Create a file name "README.md" in folder "hello-world"
   - Add new line "The first file will be commit.' into the file "README.md"
   - Use command "git status" to check status of git.
  ```
  git status
  ```
  - The out screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_example.png "repo-name")
  
2. Create new folders:
   - Create folder "files" and folder "images" in folder "hello-world" folder.
   - Use command "git status" to check status of git.
  ```
  git status
  ```
  - The out screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_example.png "git status")
  - The status is not show the two new folders "files", "images". The reason is git cannot detect the emply folders.
  - The trick is you can add a any file into folder to make folder not empty. 
  In this case I will create file ".keep" into both folders "files" and "images".
  - Let check the status now: 
  ```
  git status
  ```
  - The out screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_2.png "git status 2")
  
  - Now git can see 2 folders "files" and "images".
  
3. Add new files and folders to the index:
  - We have three new definition: your "local file", your "local git", and "git server".
    - "local file": all files in the folders.
    - "local git": you have a git on your local machine, that have some relationship with git server.
    - "git server": that you can access from the web. Example https://github.com/quangvu0702/hello-world
    <br />
    Don't be panic. I will give you examples now:
  - Remember we have a folder hello-world contains: <br />
    - README.md 
    - files/.keep
    - images/.keep
  - We have index files before moving files from "local file" to "local git". In this "hello-world" folder we have 3 files: "README.md", 
  "files/.keep", "images/.keep". We just want to index one file "README.md". We index file "README.md" to "local git"
  ```
  git add README.md
  ```
  - Let check the status now: 
  ```
  git status
  ```
  - The out screen wil be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_3.png "git status 3")
  - File "README.md" have been indexed and tracked by git. You can see 2 untracked files are "files/" and "images/".
  This mean all files in folders "files/" and "images/" are untracked. 
  This mean "local git" don't know anything about these files -  don't know there contents, whether they are changed or not.
  - Commit new files and folders to you local git: 
  after index files, we copy your indexed files to the "local repo" or "local git".
  ```
  git commit -m "This is a basic commit message."
  ```
  - Let check the status now: 
  ```
  git status
  ```
  - The out screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_status_4.png "git status 4")
  
4. Push your files and folder to server git
  - Now your "local git" have file "README.md". Let go to web and check our repo on "git server". 
  Example my git repo is: https://github.com/quangvu0702/hello-world
  My screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server.png "git server 4")
  - You can see that our "hello-world" is empty. There is no file "README.md". 
  Because we have justed commited the file "hello-world" to "local git".
  We not push "local git" to "git server" yet.
  - Now we push "local git" to "git server": (you will be asked for username and password)
  ```
  git push origin master
  ```
  - Now your "local git" have pushed to "git server". Let go to web and check our repo on "git server" again. 
  Example my git repo is: https://github.com/quangvu0702/hello-world
  My screen will be: <br />
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/git_server_2.png "git server 2")
  - Now you can see file "README.md" in your repository.
  
