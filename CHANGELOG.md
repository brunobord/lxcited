# lxcited changelog

## master

- Documentation: How to install this, trust me. How to install this for ``sudo`` usage.

## v2.1 (2015-09-11)

### Features

* Contextual autocompletion: commands to be executed on a running container only list running containers when trying to autocomplete. Same for commands like `start` to be executed only on stopped containers. Neutral commands will list all available containers (#10),
* Contextual autocomplete: autocompletion for `stop` command adds the `all` option.
* Option for ``share``, ``unshare``, ``editconfig``: use the ``--restart`` option to restart your container right after the end of the command (#9),
* Resolve relative source paths in ``push``, ``share``, ``unshare`` ; thx @lisael,
* Added a ``CONTRIBUTING.md`` file to help contributors.

## v2.0 (2015-09-02)

### New commands

* `push`: to copy a file into your container (#1),
* `share`: to share a directory via lxc.mount (#2).
* `unshare`: to unshare a directory previously mounted (#3),
* `stop all`: to stop all running containers (#6),
* `exec`: to run commands in a running container (#8).

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
