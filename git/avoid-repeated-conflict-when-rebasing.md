# Avoid Repeated Conflict when Rebasing



When using rebase we often end up having to resolve the same conflict again and again (every time we do a new rebase on an updated `master`). To avoid this we can use git `rerere` (reuse recorded resolution).

We need to set two settings:

1. `rerere.enabled 1`
   enables rerere so git remembers previous conflict resolutions

2. `rerere.autoupdate true` 
   makes git automatically stage the file after (recorded) conflict resolution is applied.

### Global

```sh
git config --global rerere.enabled 1
git config --global rerere.autoupdate true
```



### Local

```sh
git config --local rerere.enabled 1
git config --local rerere.autoupdate true
```



### Branch

Add the following to your `.git/config` file (local) or `$HOME/.gitconfig` file (global)

```sh
[includeIf "onbranch:development"]
  path=extras
```

and then put your additional settings in `.git/extras`:

```sh
[rerere]
	enabled = 1
  autoupdate = true
```



### Wrong Merge

If we do a wong merge we can `forget` the confligt resolution (merge) with

```sh
git rerere forget path/to/files
```





Sources:

https://stackoverflow.com/questions/7241678/how-to-prevent-many-git-conflicts-when-rebasing-many-commits

https://stackoverflow.com/questions/3283670/have-git-rerere-automatically-mark-files-as-resolved

https://stackoverflow.com/questions/49827353/using-gitconfig-per-branch

http://scottchacon.com/2010/03/08/rerere.html

