# Git Force Pull



If you want to pull changes from remote and overwrite local changes do

```sh
git fetch --all
git branch backup-master # Backup branch
git reset --hard origin/master
```

