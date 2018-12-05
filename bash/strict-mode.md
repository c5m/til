# Bash Strict Mode
Use the following to set bash safe mode:
```bash
if test "$BASH" = "" || "$BASH" -uc "a=();true \"\${a[@]}\"" 2>/dev/null; then
    # Bash 4.4, Zsh
    set -euo pipefail
else
    # Bash 4.3 and older chokes on empty arrays with set -u.
    set -eo pipefail
fi
shopt -s nullglob globstar
```
Setting strict mode makes your script fail immediately and loudly  
(this is good - it prevents hidden bugs).  

Here is an explanation of the settings: <br>
`-e`  exit immediately if any command fail (has a non-zero exit code) <br>
`-u` fail when referencing unset variable (one you haven't set previously) <br>
`-o pipefail` fail if any command in a pipeline fails (default is to only look at the last command) <br>
`shopt -s nullglob` makes _`for f in *.txt`_ work correctly when _`*.txt`_ matches zero files <br>
`globstar` makes globbing recursive (i.e. ** will then also enter subfolders)

source: http://redsymbol.net/articles/unofficial-bash-strict-mode/