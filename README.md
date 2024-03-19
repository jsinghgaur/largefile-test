
$ ls -lta
total 262740
drwxr-xr-x 1 91955 197609         0 Mar 20 01:19  .git/
drwxr-xr-x 1 91955 197609         0 Mar 20 01:18  ./
-rw-r--r-- 1 91955 197609 269039228 Mar 20 01:18 '200MB PDF File.pdf'
drwxr-xr-x 1 91955 197609         0 Mar 20 01:14  ../

$ git init
Initialized empty Git repository in F:/workspace/git-largefile/.git/

$ git status
On branch master
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitattributes
        200MB PDF File.pdf

nothing added to commit but untracked files present (use "git add" to track)

$ git add .

$ git commit -m "1st commit"
[master (root-commit) d24febd] 1st commit
 2 files changed, 4 insertions(+)
 create mode 100644 .gitattributes
 create mode 100644 200MB PDF File.pdf


$ git lfs install
Updated Git hooks.
Git LFS initialized.


$ git lfs track "*.pdf"
Tracking "*.pdf"

$ git remote add origin <github repository url>


$ git lfs push --all origin master
Uploading LFS objects: 100% (1/1), 269 MB | 923 KB/s, done.

$ git push -u origin master
Uploading LFS objects: 100% (1/1), 269 MB | 0 B/s, done.
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 415 bytes | 207.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/jsinghgaur/largefile-test.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.


NOTE 
++++
$ git lfs push --all origin master
exit status 1
Error getting local refs.

--> If you are getting this error, it means you have something uncommited in your local repository




