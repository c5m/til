# Diff Against Files in Specific Folder

To get at list of files changed in a given folder (compared to `master`)

```sh
git diff --name-only master -- path/to/folder/
```



To diff `master` against any folder do

```sh
git diff --name-only master..branch -- path/to/folder/
```

