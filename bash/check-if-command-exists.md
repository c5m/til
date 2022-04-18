# Check if Command Exists

To check if a *command* exists (such as `git`) use the following (it is POSIX compliant)

```sh
if ! command -v <your_command> &> /dev/null
then
    echo "<your_command> could not be found"
    exit
fi
```

