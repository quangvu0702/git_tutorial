# Introduction
   - Create git account on https://github.com.
   - Create a new repository on git. 
   - Download you repository to your local machine.
   - (Option) Add public key to your git account - Git will not request you username add password every time you push or commit after you add your public key.
   
1. Create git account on https://github.com: 
   - Go to https://github.com the sign up an account. Email and password.
   
2. Create a new repository name "hello-world" on git:
   - In the upper-right corner of any page, click , and then click New repository. ![](https://help.github.com/assets/images/help/repository/repo-create.png "repo-create")
   
   - Type a name for your repository - we use name "hello-world", and an optional description.![](https://help.github.com/assets/images/help/repository/create-repository-name.png "repo-name")
   
   - When you're finished, click "Create repository".
   
3. Download you repository to your local machine:
   - First you have to install git on you machine.
     - Windows: https://www.atlassian.com/git/tutorials/install-git#windows
     - Linus: https://www.atlassian.com/git/tutorials/install-git#linux
     - Mac: https://www.atlassian.com/git/tutorials/install-git#mac-os-x
   - Clone you repository you have create on step 2 name "hello-world" to you local machine:
     - Remember you have to set your username and email: user your name replace to "Emma Paris" and you email replace to 
     "eparis@atlassian.com". <br /> Example: git config --global user.name "David", git config --global user.email "david@gmail.com"
     ```
     git config --global user.name "Emma Paris"
     git config --global user.email "eparis@atlassian.com"
     ```
     ```
     git clone https://github.com/quangvu0702/hello-world.git
     ```
     - You wil be asked for password. Please enter you password.
     - Now you have a folder named "hello-world" in you local machine.
     
 4. Optional(Add public key to your git):
    - Being asked password every time we work with git server is very annoy. We need a way to tell git server who we are so it will not asked who we are every time. ("public key" - "private key") is a way to do that. 
    - In this case, you can see "public key" is a lock and "private key" is a key. You will give git server "public key" yes it is "public key" that key is public. That is no harm if people know you public key. After git server know you "public_key", it will auto looking for your "private_key" on a default folder and check whether "private_key" can open a "public_key" that it holding. No passwork needed.
    - Remember if other people have your "private_key" they can modify your git freely so make "private_key" private.
    - For more information please go to offical link: https://help.github.com/articles/connecting-to-github-with-ssh/
    
    - Windows: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows
    - Mac: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-mac
    - Linus: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux
