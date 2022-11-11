# Fetch a Different Branch than the Current

To `git fetch` a different branch than the one you are currently on use: 

```sh
git fetch origin master:master
```

If you want to merge the changes in `origin` into the current just do:

```sh
git merge master
```

