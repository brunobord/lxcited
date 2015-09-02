# lxcited changelog

## master (unreleased)

### New commands

* `push`: to copy a file into your container (#1),
* `share`: to share a directory via lxc.mount (#2).

### Other niceties

* `help` function has been revamped & multiline help text for more information and readability (#4),
* `help` function now accepts a ``[command]`` argument, to get help on a specific command (#7),
* removed `check` from help. It has never been a command in the first place.

## v1.0 (2015-08-26)

First release! Yay!

### Available commands

* `init`: create a container based on a template,
* `ls`: list available containers (fancy list),
* `start`: start your container,
* `stop`: stop your container,
* `restart`: restart your container,
* `attach`: attach to a running container,
* `go`: start & attach to your container,
* `info`: give information about a named container,
* `ip`: give the IP address of a running container,
* `editconfig`: open the container configuration file in you ``$EDITOR``,
* `destroy`: delete your container (good bye),
* `help`: gives help and usage instructions.

### Other niceties

* Easy to setup (copy-paste files in your path, edit your bash profile file),
* Autocompletion for commands and containers,
* Will only run if you're root (su or sudo),
* WTFPL,
* a cool name found by @GreatWizard.
