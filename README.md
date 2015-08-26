# LXCited

A bash-based remote control for LXC containers.

This script goal is to ease the common tasks when controlling LXC containers on a machine.

Why this? because is a [PITA](https://en.wiktionary.org/wiki/PITA) to constantly type the ``--name`` option while you *need* it (so it's not an option, it should be a mandatory argument for ``lxc-*`` commands).

## Install

It's a manual install. Don't worry, there aren't any hard step.

1. Copy the ``lxcited`` file somewhere in your ``$PATH``,
2. make sure it's executable (use ``chmod`` if necessary),
3. Copy the ``lxcited.autocomplete`` file somewhere,
4. Add the following to your ``.bashrc`` or ``.bash_profile``:

```sh
source /path/to/lxcited.autocomplete
```


## Usage

**WARNING**: you **have** to be root to use this tool.

```sh
lxcited COMMAND
```

For example:

```sh
lxcited start what_a_beautiful_container
```

Get help with:

```sh
lxcited help
```

### Autocomplete

You can autocomplete commands:

```
$ lxcited st<TAB><TAB>
start stop
$ lxcited st
```

... or containers:

```
$ lxcited start deb<TAB><TAB>
debian1 debian2 deborah
$ lxcited start deb
```

## License

This piece of software is published under the terms of the WTFPL

See: http://www.wtfpl.net/ for more details, but here is its core term:

   0. You just DO WHAT THE FUCK YOU WANT TO.
