
-----------------------------------------------------------------
			Tutorial for git_command
----------------------------------------------------------------

1. Create remote reposity in github.com to store source code pushed from local machine
(laptop).
   Ex: https://github.com/Hohungduy/openwrt_luci

2. Create local folder to store code in our local machine. This folder will connect with our repository.

3. Enter the folder, then:
 -- initiate git in this folder
     `git init`
 
 -- Connect and link this folder with repository in github
     `git remote add origin https://github.com/Hohungduy/openwrt_luci`

 -- Pull all content and code from repository from github
     `git pull origin master`

4. When we have change in local folder, we have to update repository
 -- First, add folder or file
    Ex: `git add luci_static/`
 -- Then, we have to commit this change and add a comment
    EX: `git commit -m "Add luci theme with new Materialand Rosy theme"`
 -- Finally, we have to push it
    EX: `git push origin master`
 -- Enter username and password
    Username: duyhohung.work@gmail.com
    Password: Duy**********

5. Create branch
 -- First, we have master. To create other branches, we do:
    EX: `git checkout -b xxxx`
    xxxx is a name of this new branch
 -- To switch to master branch, we do
    Ex: `git checkout master`
 -- To delete the branch, we do:
    `git branch -d xxxx`
 -- To merge other branches to current branch (ex: master)
    `git merge xxxx`
 -- Before we merge, we can preview by:
    `git diff <origin_branch> <dest_branch>`
 -- To destroy all change  and come back to the nearest history point in remote
 and assign local master into this
    `git fetch origin`
    `git reset --hard origin/master`
-----------------------------------------------------------------------------------
***NOTE: 
   To clone 1 repository which is available on github
    
   git clone /path/repository

   If this repository in other server /remote, we do:

   git clone username@remote_address:/path/repository

 
----------------------------------------------------------------
Author: Duy Ho
Email : duyhohung.work@gmail.com
---------------------------------------------------------------


