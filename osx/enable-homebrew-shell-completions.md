# Enable Homebrew Shell Completions

Homebrew sometimes comes with shell completions which is installed in
`/opt/homebrew/share/zsh/site-functions` folder

To enable these in ZSH add the follwing to your `.zprofile`

```sh
FPATH="$(brew --prefix)/share/zsh/site-functions:${FPATH}"
```

For more details see Homebrews [manual](https://docs.brew.sh/Shell-Completion#configuring-completions-in-zsh)

