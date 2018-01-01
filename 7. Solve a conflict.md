# Solve a conflict
  - A conflict will be exist when git don't know how to merge files.
  - We need to merge files manually.
1 Merge the "master" branch into "hello-two":
  - We want to create a pull request from the "hello-two" branch into the "master" branch.
  - There is a conflict on "hello.txt" file when we create a pull request. Git don't how to merge "hello.txt" file.
  - We haev to merge this file manually.
  - Run:
  ```
  git checkout hello-two
  git merge master
  ```
  - Output:
  ```
  $ git checkout hello-two
  Switched to branch 'hello-two'
  $ git merge master
  Auto-merging hello.txt
  CONFLICT (content): Merge conflict in hello.txt
  Automatic merge failed; fix conflicts and then commit the result.
  ```
  - If you open the hello.txt you will see:
  ```
  "Hello"
  <<<<<<< HEAD
  Hello from branch named hello-two!!!
  =======
  Sorry I cannot hear you!
  >>>>>>> master
  Hello, it's me
  I was wondering if after all these years you'd like to meet
  To go over everything
  They say that time's supposed to heal ya
  ...
  ```
2 Merge the conficted file manually:
  - Git will tell you the lines which git cannot auto merge.
  - In this case, the second line of "hello.txt" in "hello-two" branch:
  ```
  Hello from branch named hello-two!!!
  ```
  - And the second line of "hello.txt" in "master" branch: 
  ```
  Sorry I cannot hear you!
  ```
  - Git will tell you by syntact:
  ```
  <<<<<<< HEAD
  Hello from branch named hello-two!!!
  =======
  Sorry I cannot hear you!
  >>>>>>> master
  ```
3 Resolution of the conflict:
  - We have to edit file to solve conflict. I decide to keep 2 lines and add one more line into the "hello.txt" file.
  - Edit:
  ```
  "Hello"
  Hello from branch named hello-two!!!
  Keep both lines.
  Sorry I cannot hear you!
  Hello, it's me
  I was wondering if after all these years you'd like to meet
  To go over everything
  ...
  ```
4 Make a commit of conflict resolution:
  Run:
  ```
  git add hello.txt
  git commit -m "Merged master fixed conflict."
  git push origin hello-two
  ```
  - We have solved the conflict. 
  
5 Let create a pull request from "hello-two" to "master" branch again. We won't see any confict.
  - Create a pull request.
  - Merge this pull request to "master" branch.
  
