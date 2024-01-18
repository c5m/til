# Diff Filename Only
To see only the filename of what changed between two commits use:

```
git diff --name-only <ref_1> <ref_2>
```



If we want only the filenames (without path) do

```sh
git diff --name-only master | awk -F '/' '{print $NF}' | sort | uniq
```

