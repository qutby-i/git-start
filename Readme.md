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
```