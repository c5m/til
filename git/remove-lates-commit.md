# Remove Lates Commit
To remove a commit you have just done do a **soft** reset to ```HEAD~1``` as this

```
git reset --soft HEAD~1
```

This will keep the changes in the file.

To delete the changes from the file do a **hard** reset instead

```
git reset --hard HEAD~1
```