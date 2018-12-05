# .bashrc vs .profile

**Shell types**

**Interactive**: As the term implies: Interactive means that the commands are run with user-interaction from keyboard. E.g. the shell can prompt the user to enter input.

**Non-interactive**: the shell is probably run from an automated process so it can't assume if can request input or that someone will see the output. E.g Maybe it is best to write output to a log-file.

**Login**: Means that the shell is run as part of the login of the user to the system. Typically used to do any configuration that a user needs/wants to establish his work-environment.

**Non-login**: Any other shell run by the user after logging on, or which is run by any automated process which is not coupled to a logged in user.

**TL;DR:**
* `~/.bash_profile` should be super-simple and just load .profile and .bashrc (in that order)
* `~/.profile` has the stuff NOT specifically related to bash, such as environment variables (PATH and friends)
* `~/.bashrc` has anything you'd want at an interactive command line. Command prompt, EDITOR variable, bash aliases for my use

**A few other notes:**
* Anything that should be available to graphical applications OR to sh (or bash invoked as `sh`) MUST be in `~/.profile`
* `~/.bashrc` must not output anything
* Anything that should be available only to login shells should go in `~/.profile`
* Ensure that `~/.bash_login` does not exist.