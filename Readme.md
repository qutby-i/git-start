# git-start
Starting to exprement with git


## git local -> remote history
```zsh
➜  git-start git:(br-news) git pull origin br-news --allow-unrelated-histories
From https://github.com/qutby-i/git-start
 * branch            br-news    -> FETCH_HEAD
Merge made by the 'ort' strategy.
 .gitignore | 136 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 LICENSE    |  21 ++++++++++
 README.md  |   2 +
 3 files changed, 159 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 LICENSE
 create mode 100644 README.md
 ## Pull from terminal/local
 ➜  git-start git:(master) git pull -v    
POST git-upload-pack (227 bytes)
POST git-upload-pack (376 bytes)
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (5/5), 1.32 KiB | 45.00 KiB/s, done.
From https://github.com/qutby-i/git-start        
   5b5d313..bf5454f  br-news    -> origin/br-news
 = [up to date]      master     -> origin/master
Updating 5b5d313..bf5454f
Fast-forward
 src/html/news.html | 19 +++++++++++++++++--
 1 file changed, 17 insertions(+), 2 deletions(-)
```