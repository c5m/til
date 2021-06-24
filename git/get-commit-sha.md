# Git Get Commit SHA

To get the commit SHA (of HEAD) use

```sh
git rev-parse HEAD
```

to get he short version use

```sh
git rev-parse --short HEAD
```

and if you want to specify a length use

```sh
git rev-parse --short=10 HEAD
```

note that if you ask for a very short SHA (i.e n=2), git will give you the shortest possible SHA that is distinguishable from other commit SHAs (probably n=4).

