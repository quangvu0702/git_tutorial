# Create a pull request
  - When we want to merge a branch into another branch, we will create a pull request.
  - In this example we have the branch named "hello-adele" with the file 'hello.txt'. We want to merge this branch to branch "master".
1. Create a pull request:

   - We go to "server git" on our browser. In my case it is "https://github.com/quangvu0702/hello-world". 
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR1.png "PR1")
   - We can see that we have two branches. Click on the link inside the green cicle as in the image to see which branches we have.
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR2.png "PR2")
   - We are having two branches: "master" and "hello-adele".
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR2.png "PR2")
   - Now we want to merge branch "hello-adele" into branch "master". Click on branch "hello-adele" as image bellow.
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR3.png "PR2")
   - We go to branch "hello-adele":
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR4.png "PR2")
   - We can see the button "New pull Request". Click on the button to create a pull request. This is the output image.
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR5.png "PR2")
   - We can see the button "Create pull request". Click on that button to create a pull request. This is the output image.
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR6.png "PR2")
   - If we have full right to the repository we will see the button "Merge pull request".
   - Click on the button "Merge pull request" to merge the branch "hello-adele" to "master":
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/PR7.png "PR2")
   - These are all the steps to create a pull request.
2. Update "local git" after merging pull request:
   - We have just merged branch "hello-adele" to "master".
   - Let's "checkout" to branch "master"
   ```
   git checkout master
   ```
   - And check contents of the folder "hello-world": we only see one file README.md. Where is file "hello.txt"?
   - The "pull request" only effects "server git". The contents have only been updated in "server git". We have to update our "local git" by command:
   ```
   git pull origin master
   ```
   - We can see that the file "hello.txt" is now in our local machine.
