# Introduction
   - Create a git account on https://github.com.
   - Create a new repository on git. 
   - Download you repository to your local machine.
   - (Optional) Add public key to your git account - Git will not request your username and password every time you push or commit after you add your public key.
   
1. Create a git account on https://github.com: 
   - Go to https://github.com to sign up an account. 
   
2. Create a new repository name "hello-world" on git:
   - In the upper-right corner of any page, click on the arrow down and then click "New repository". ![](https://help.github.com/assets/images/help/repository/repo-create.png "repo-create")
   
   - Type a name for your repository - here we use "hello-world". You can add a description (optional).![](https://help.github.com/assets/images/help/repository/create-repository-name.png "repo-name")
   
   - When you're finished, click "Create repository".
   
3. Download you repository to your local machine:
   - First you have to install git on your machine.
     - Windows: https://www.atlassian.com/git/tutorials/install-git#windows
     - Linus: https://www.atlassian.com/git/tutorials/install-git#linux
     - Mac: https://www.atlassian.com/git/tutorials/install-git#mac-os-x
   - Clone the repository "hello-world" you have created at step 2 to your local machine:
     - Remember that you have to set your username and email: user your name in place of "Emma Paris" and your email in place of
     "eparis@atlassian.com". <br /> Example: git config --global user.name "David", git config --global user.email "david@gmail.com"
     ```
     git config --global user.name "Emma Paris"
     git config --global user.email "eparis@atlassian.com"
     ```
     ```
     git clone https://github.com/quangvu0702/hello-world.git
     ```
     - You wil be asked for password. Please enter your password.
     - Now you have a folder named "hello-world" in your local machine.
     
 4. Optional (Add public key to your git):
    - Being asked for password every time we work with git server is very annoying. We need a way to tell git server who we are so it will not repeat the question everytime we work with git server."public key" - "private key" is a way to do that. 
    - In this case, you can see "public key" ass a lock and "private key" as a key. You will give git server the "public key". The key is public so there is no harm if people know you public key. After git server know you "public_key", it will auto-look for your "private_key" on a default folder and check whether "private_key" can open the "public_key" that it is holding. No password is needed.
    - Remember that if other people have your "private_key" they can modify your git without any restriction so make your "private_key" private.
    - For more information please go to the offical link: https://help.github.com/articles/connecting-to-github-with-ssh/
    
    - Windows: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows
    - Mac: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-mac
    - Linus: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux
