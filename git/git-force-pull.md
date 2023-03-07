# Git Force Pull



If you want to pull changes from remote and overwrite local changes do



```sh
git fetch
git reset --hard HEAD
git merge '@{u}'
```

