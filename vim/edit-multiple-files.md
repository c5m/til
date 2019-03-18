# Edit Multiple Files in Vim

To edit multiple files in Vim (one after another) first open the files with

```sh
vim foo.txt bar.txt
```

Then we can navigate between the files with

```txt
:n 		- navigate to next file
:wn 	- write and navigate to next file
:prev 	- navigate to previous file
```

To see what file you are in use `:args`

```sh
[foo.txt] bar.txt
```

