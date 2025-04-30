# README.MD

```zsh
➜  git-start git:(master) echo "# README.MD" > Readme.md  | git hash-object Readme.md -w
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it    
4747ae5ca7d495aaedc93afc3edc4db84a67d956
## Type of Readme.md
\➜  git-start git:(master) ✗git cat-file -t 4747ae5ca7d495aaedc93afc3edc4db84a67d956
blob
## Making Tree not this way!!! 
\➜  git-start git:(master) ✗git hash-object ../tmp-tree.txt 
3bb789e0eefa7341bb4ea7a744d1ef5b9f954f86
## That way 
➜  git-start git:(master) ✗ cat ../tmp-tree.txt | git mktree
f68ed23a339ddd98407eaa95884d8e55a39f536e
## Tree-Object Content
\➜  git-start git:(master) ✗git cat-file -p f68ed23a339ddd98407eaa95884d8e55a39f536e
100644 blob c2eac0b8bff290969eacbffd52ceeb4290390e11    gitLovers.md
100644 blob b7aec520dec0a7516c18eb4c68b64ae1eb9b5a5e    hellogit.txt
## Tree-Object Type
\➜  git-start git:(master) ✗git cat-file -t f68ed23a339ddd98407eaa95884d8e55a39f536e
tree
## Tree-Object Size
\➜  git-start git:(master) ✗git cat-file -s f68ed23a339ddd98407eaa95884d8e55a39f536e
80
##
➜  git-start git:(master) git log
\➜  git-start git:(master)git status
On branch master
nothing to commit, working tree clean
\➜  git-start git:(master)git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        main.js
        style.css

nothing added to commit but untracked files present (use "git add" to track)
➜  git-start git:(master) ✗ git add .
\➜  git-start git:(master) ✗git commit -m "Added some files"
[master 4cad5ca] Added some files 
 3 files changed, 34 insertions(+)
 create mode 100644 index.html    
 create mode 100644 main.js       
 create mode 100644 style.css   
## List Branches verbose
➜  git-start git:(master) git branch -v
* master 4cad5ca Added some files
(END)
##
➜  git-start git:(master) git branch br-links
➜  git-start git:(master) git branch -a
➜  git-start git:(master) git checkout br-links
Switched to branch 'br-links'
➜  git-start git:(br-links)
##
\➜  git-start git:(br-links) git cat-file -p 510b1e359286352246 
tree e31fd4abe3473375f78fdd48b35c095a2a68d3f9
parent 4cad5ca0c31ceb4871e4b6afbb4e4a2326c8ff52
author qutby-i <kutbiay@yahoo.de> 1746029116 +0200
committer qutby-i <kutbiay@yahoo.de> 1746029116 +0200

Added home.html with perfect content
\➜  git-start git:(br-links) git cat-file -p master             
tree d74c282efe680b0dcd5f3dcefc328fa8c2728ed8
parent 85feb19343714da744327c6ee6805c60cc601315
author qutby-i <kutbiay@yahoo.de> 1746028528 +0200
committer qutby-i <kutbiay@yahoo.de> 1746028528 +0200

Added some files
\➜  git-start git:(br-links) git cat-file t master 
commit
\➜  git-start git:(br-links) git cat-file -t d74c282efe68
tree
\➜  git-start git:(br-links) git cat-file p d74c282efe68
100644 blob 483a6a0a7c4b86e412fed1447825c6d759f28359    Readme.md
100644 blob b990aa251c62e3e756be7a9441acb75ad46c206e    index.html
100644 blob 00c834d47cee06a8ea12880fcafd4f9ec9f24a18    main.js
100644 blob 91388a5f90d53d954be448eab2b72f0d12b137cf    style.css

```