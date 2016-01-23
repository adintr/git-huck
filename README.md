# git-huck

  a group of script tools make git easier to use. (git-huck 是一组更方便使用 git 的脚本工具)

###INSTALL (安装)
```
git clone https://github.com/adintr/git-huck.git git-huck
cd git-huck
./install.sh
```

### Addtion Commands: (扩展的命令)
1. apply-topic [MIP]

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

2. git mulpush, git mulpull

  for each added remote repository, run git push/pull on it. (对每一个添加的远程仓库使用 git push/pull 命令)

