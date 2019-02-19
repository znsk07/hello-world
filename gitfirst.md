definition:
     repositary  eq to  a local folder + git init
                 eq to workspace  eq to local folder + vscode init
steps to using git in vscode
1. create a local repositary 
          create a local folder, in this example is CSC002
          open terminal in CSC002, run >git init 
          to activate(label) the directory is a git repositary
          (it creates .git/ folder(hidden)in CSC002),
          edit .git/config to define remote origin
                              define branch master
         git remote add origin https://github.com/znsk07/hello-world
         git pull origin version1
like this the content of .git/config
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
        ignorecase = true
        precomposeunicode = true
[remote "origin"]      #added by git remote add origin https://aaaaa
        url = https://github.com/znsk07/hello-world
        fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]       #added by git pull origin master
        remote = origin
        merge = refs/heads/master
[branch "version1"]
        remote = origin
        merge = refs/heads/version1
SellinaLudeMacBook-Pro:.git sellina$ 


second method to create local repositary
using git clone to clone a remote repositary to local directory as local repositary

git clone https://github.com/znsk07/2nd-github.git   
# create a local folder 2nd-github on local workspage
#to check the config in its hidden .git directory
# add a local file first.md in to the folder 2nd-github
#open terminal on local folder 2nd-github
undter newly cloned local repositary, create a local file, edit it then
using 'git add' the file to working cache
using 'git commit' to commit the changes
using 'git push origin master' to merge local committed statged file to remote brach master

git add first.md
git commit -m "add my first.md to repositary"
git push origin master
#push local repositary to remote repositary and merger into master
#origin means remote https://github.com/znsk07/2nd-github.git
#master means the first branch in origin (which is 2nd-github.git)

seems I can only create new branch on github.com site.
can't create new branch on local repositary

next question, change a new branch in 2nd-github.git, new branch-name is date-version
# and then push committed changes to new branch
my personal access token to github [under developing section of github settings]

b3921551b9cc162077f8c703c028c666a8a1662e
