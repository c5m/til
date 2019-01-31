# Vim Read from Stdin

To have Vim read form `stdin` use:

```sh
<command> | vim -R -
```


The `-` at the end is what tells Vim to read from `stdin`.
The flag `-R` makes vim *read only* which is needed to make Vim quit correctly on `:q`
(otherwise Vim will complain about `No write since last change ...`).