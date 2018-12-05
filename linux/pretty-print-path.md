# Pretty Print PATH 
The following command will split `$PATH` on `:` and print each entry on a new line

```sh
echo $PATH | sed 's/:/\n/g'
```
