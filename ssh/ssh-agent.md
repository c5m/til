# SSH Agent

To start an agent and add the key do
```sh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/<key-file>
```
if your key is the standard `id_rsa` the path can be omitted.

It is considered good pratice to put a time limit on how long your keys will stay in memory.   
This can be done with the `-t <seconds>` flag.

## Windows

To have the `ssh-agent` auto-launch on Windows add the following
to your `.bashrc`
```sh
env=~/.ssh/agent.env

agent_load_env () { test -f "$env" && . "$env" >| /dev/null ; }

agent_start () {
    (umask 077; ssh-agent >| "$env")
    . "$env" >| /dev/null ; }

agent_load_env

# agent_run_state: 0=agent running w/ key; 1=agent w/o key; 2= agent not running
agent_run_state=$(ssh-add -l >| /dev/null 2>&1; echo $?)

if [ ! "$SSH_AUTH_SOCK" ] || [ $agent_run_state = 2 ]; then
    agent_start
    ssh-add
elif [ "$SSH_AUTH_SOCK" ] && [ $agent_run_state = 1 ]; then
    ssh-add
fi

unset env
```
[source](https://help.github.com/articles/working-with-ssh-key-passphrases/#auto-launching-ssh-agent-on-git-for-windows)