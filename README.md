# git-huck

  a group of script tools make git easier to use. (git-huck 是一组更方便使用 git 的脚本工具)

### INSTALL (安装)
```
git clone https://github.com/adintr/git-huck.git git-huck
cd git-huck
./install.sh
```

### Addtion Commands: (扩展的命令)
1. apply-topic

  apply the current topic branch to all master(thunk) branchs. example:
  ![branchs now](https://raw.githubusercontent.com/adintr/git-huck/master/doc_images/branchs_before.jpg)
  ```
  git apply-topic master1 master2 master3
  ```
  or
  ```
  git config huck.masters  "master1 master2 master3"   (do this only once)
  git apply-topic
  ```
  now we get:
  ![branchs now](https://raw.githubusercontent.com/adintr/git-huck/master/doc_images/branchs_after.jpg)
  
  More:
    ```
    git config huck.keyword <keyword>
    ```
    will only pick commit which include keyword as message to target branchs.

  ```
  git apply-topic --continue
  ```
  if some conflict in merge, after solve it, use this to continue.
  
2. git mulpush, git mulpull

  for each added remote repository, run git push/pull on it. (对每一个添加的远程仓库使用 git push/pull 命令)
  ```
  git config huck.push.<remote_repository>  "loc_branch1:remote_branch1 loc_branch2:remote_branch2 ..."
  ```
  config the branch to push for each respository. (配置每一个远程仓库需要 push 的分支)

3. git view
  open the file of the given commit. (打开指定的版本中的文件)
  ```
  git view <commit object>  <file path>
  ```
