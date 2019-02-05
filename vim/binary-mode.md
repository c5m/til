# Vim in Binary Mode

To make Vim display a file in binary mode use

```
:e ++bin
```

This allows us to see if the file has a Unicode byte order mark

(i.e if the files starts with `<feff>` for instance).

This can be helpful when debugging issues with `csv` files.