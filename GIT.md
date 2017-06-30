GitHub supports:
- The import of Git, SVN, HG, TFS.

GitLab supports: 
- The import of Git.
- Easy import from other services GitHub, Bitbucket, Google Code, Fogbugz.

Coding supports: 
- The import of Git, SVN, HG.

Bitbucket supports:
- The import of Git, CodePlex, Google Code, HG, SourceForge, SVN.

https://guides.github.com/activities/hello-world/

####  Add changes to new repository on the command line

echo "# ChromeExtTypescriptForStarter" >> README.md
git init 
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/AAcoder/ChromeExtTypescriptForStarter.git
git push -u origin master

HTTPS
git remote add origin https://github.com/AAcoder/ChromeExtTypescriptForStarter.git

SSH
git remote add origin git@github.com:abhiagg123/testing.git
git remote add origin git@bitbucket.org:abhiagg123/XamarinBasicApp.git

####  Remove remote repo linking

git remote rm origin

####  View Remote branch

git remote -v

####  GIT Commit

git commit -m "first commit"


Git 
lets say u need to add new feature/prototype
create new branch from existing

#### once changes completed move all changes from temp branch back to main branch
$ git push <remote> <local branch name>:<remote branch to push into>
$ git push origin tempBranch:master

......................................................................................
Git tip: Tired of entering password again and again ?

Run this command to remember your password:
git config --global credential.helper 'cache --timeout 28800'
Above command will tell git to cache your password for 8 hours.

How to make git forget this password ?
If you want to switch to another github account then u can run this command
git credential-cache exit
Above command will flush any stored password from cache.

Reference: http://git-scm.com/docs/git-credential-cache

Windows User ?
git config --global credential.helper wincred

.............................................................................

