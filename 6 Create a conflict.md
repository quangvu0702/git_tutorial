# Create a conflict
  - A conflict exsits when there are many modifications on a file from many branches.
  - In this example we create two new branches "hello-one" and "hello-two". 
  - We will modify the file named "hello.txt" on branch "hello-one", create a pull request to branch "master" and merge to branch "master".
  - Then we modify the file named "hello.txt" on the line that is modified by branch "hello-one" on branch "hello-two", create a pull request to branch "master", in this case we will see a confict.
1 Create two branches:
  - Change working branch to master:
  ```
  git checkout master
  ```
  - Create branch "hello-one"
  ```
  git checkout -b hello-one
  ```
  - Working branch is "hello-one" now. Change working branch to master again:
  ```
  git checkout master
  ```
  - Create branch "hello-two"
  ```
  git checkout -b hello-two
  ```
  - Working branch is "hello-two" now. Change working branch to "hello-one":
  ```
  git checkout hello-one
  ```
  - Check the list of branches:
  ```
  git branch
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict1.png)
  
2 Modify the file "hello.txt" on branch "hello-one".
  - Below are the first 5 lines of file "hello.txt":
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict2.png)
  - We will modify the second line to "Sorry I cannot hear you!"
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict3.png)
  - We add file, commit and push branch "hello-one" to server git. We run the commands bellow step by step.
  ```
  git status
  git diff hello.txt
  git add hello.txt
  git commit -m "modify second line of the file named hello.txt"
  git push origin hello-one
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict4.png)
 
3 Create a pull request from branch "hello-one" to master and merge this pull request to master. (See tutorial 5 for more details)
https://github.com/quangvu0702/git_tutorial/blob/master/5%20Create%20a%20pull%20request.md

4 Change working branch to "hello-two":
  ```
  git checkout hello-two
  ```
5 Modify the file "hello.txt" on branch "hello-two":
  - This is the first 5 lines of file "hello.txt":
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict2.png)
  - We can see what we have done on branch "hello-one" does not affect this branch.
  - We will modify the second line to "Hello from branch named hello-two!!!"
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict5.png)
  - We add file, commit and push branch "hello-two" to server git. We run the commands bellow step by step.
  ```
  git status
  git diff hello.txt
  git add hello.txt
  git commit -m "modify second line of the file named hello.txt by hello-two"
  git push origin hello-two
  ```
  ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict6.png)
 6 Create a pull request from branch "hello-two" to master.
   - We can see a confict when we create a pull request: "cannot automatically merge"
   ![](https://github.com/quangvu0702/git_tutorial/blob/master/images/conflict7.png)
   - Confict exists because git doesn't know how to merge the file "hello.txt" of branch "hello-two".
   - In the next session we will solve this conflict.
 
 
