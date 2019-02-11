---
title: "Config Files"
weight: 20
---

Besides having environment variables, Linux also has some scripts which are used to control Linux environment behavior.

These scripts control Linux behavior from boot time all the way to startup and run time. You can give normal Linux commands and also complex shell scripts in these files. 

As the AP cluster uses **Bash as the default shell**, you need to understand the differences among three **config files**: `.bashrc`, `.bash_profile`, and `.profile`.

Here's the info from [bash manpage](https://linux.die.net/man/1/bash):

>When bash is invoked as an interactive **login shell**, or as a non-interactive shell with the `--login` option, it first reads and executes commands from the file `/etc/profile`, if that file exists.
>
>After reading that file, it looks for`~/.bash_profile`, `~/.bash_login`, and `~/.profile`, in that order, and reads and executes commands from the first one that exists and is readable. <br>
>The `--noprofile` option may be used when the shell is started to inhibit this behavior.
>
>When an interactive shell that is **not a login shell** is started, bash reads and executes commands from `/etc/bash.bashrc` and `~/.bashrc`, if these files exist.
>
>This may be inhibited by using the `--norc` option. <br>
>The `--rcfile` file option will force bash to read and execute commands from file instead of `/etc/bash.bashrc` and `~/.bashrc`.



- `.profile` is for things that are not specifically related to Bash, like environment variables `PATH` and friends, and should be available anytime.
- `.bashrc` is for the configuring the interactive Bash usage, like Bash aliases, setting your favorite editor, setting the Bash prompt, etc.
- `.bash_profile` is for making sure that both the things in `.profile` and `.bashrc` are loaded for login shells. You'll find most people end up telling their `.bash_profile` to also read `.bashrc` with something like `[[ -r ~/.bashrc ]] && . ~/.bashrc`

{{% notice note %}}

Config files under `/etc` directory affect behavior for **every user**, while these under `~` (HOME) directory affect behavior for only a **specific user**.

A **login shell** means a session where you log in to the system and directly end up in Bash, like a remote ssh session or logging in through a non-graphical text terminal.

A **non-login shell** is then the type of shells you open after logging in: typically in a graphical session when you open a new terminal window.

{{% /notice %}}

### Summary

![summary](https://what.thedailywtf.com/uploads/files/1462690324423-upload-f8cce917-e33c-4671-ac56-f1b0da9f687f.png)

#### *References*

1. [bashrc_and_others](https://www.stefaanlippens.net/bashrc_and_others/)
2. [My bashrc, bash aliases, profile and other files](https://www.stefaanlippens.net/my_bashrc_aliases_profile_and_other_stuff/)
3. [Choosing between .bashrc, .profile, .bash_profile, etc](https://superuser.com/questions/789448/choosing-between-bashrc-profile-bash-profile-etc)
4. [.bash_profile vs .bashrc Ubuntu](https://what.thedailywtf.com/topic/19866/bash_profile-vs-bashrc-ubuntu)