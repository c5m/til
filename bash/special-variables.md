# Special Variables in Bash



- `$1`, `$2`, `$3`, ... are the [positional parameters](https://www.gnu.org/software/bash/manual/html_node/Positional-Parameters.html).
- `"$@"` is an array-like construct of all positional parameters, `{$1, $2, $3 ...}`.
- `"$*"` is the IFS expansion of all positional parameters, `$1 $2 $3 ...`.
- `$#` is the number of positional parameters.
- `$-` current options set for the shell.
- `$$` pid of the current shell (not subshell).
- `$_` most recent parameter (or the abs path of the command to start the current shell immediately after startup).
- `$IFS` is the (input) field separator.
- `$?` is the most recent foreground pipeline exit status.
- `$!` is the PID of the most recent background command.
- `$0` is the name of the shell or shell script.

Source: https://stackoverflow.com/questions/5163144/what-are-the-special-dollar-sign-shell-variables
Official Bash Documentation: https://www.gnu.org/software/bash/manual/html_node/Special-Parameters.html
Index: https://www.gnu.org/software/bash/manual/html_node/Variable-Index.html