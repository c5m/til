# Rename files

To rename files in bash we can use

```bash
for file in *; do mv "${file}" "${file/000/}"; done
```

This removes `000` from the filename.

To experiment replace `mv` with `echo`.

(for info on the bash parameter expansion see: https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Shell-Parameter-Expansion)



**Alternatively** we can use the `rename` tool

```bash
rename 's/000//g' *000*
```

This renames all files in the current directory.

There is a `--dry-run` option which can be used to experiment.

To rename recursively in subdirectories as well combine with `find`

```bash
find . -name "*000*" | rename 's/000//g'
```

