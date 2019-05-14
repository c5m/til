# Rename Remote Branch

### 1. Rename local branch

If we already are on the branch we want to rename:

```sh
git branch -m new-name
```



If we are on another branch than the one we want to rename:

```sh
git branch -m old-name new-name
```



### 2. Delete old remote branch and push new

```sh
git push origin :old-name new-name
```

(the colon `:`  signifies an empty source ref thereby making git implicitly delete the old branch)



### 3. Reset upstream branch for new branch

Make sure you are on the new branch, then:

```sh
git push origin -u new-name
```

