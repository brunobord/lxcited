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

### Trust me on this

This will install the latest master version of lxcited in your home environment.

```sh
mkdir -p ~/bin
curl -o ~/bin/lxcited https://raw.githubusercontent.com/brunobord/lxcited/master/lxcited
curl -o ~/bin/lxcited.autocomplete https://raw.githubusercontent.com/brunobord/lxcited/master/lxcited.autocomplete
chmod +x ~/bin/lxcited
echo '# LXCITED' >> .bashrc
echo 'export PATH=$HOME/bin/:$PATH' >> .bashrc
echo 'source $HOME/bin/lxcited.autocomplete' >> .bashrc
```

Next time you'll run "source .bashrc" (manually or when you'll log in), `lxcited` will be available.

If you want to simply update, just re-rerun the two cURL commands.

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

For more help on a specific command, simply type:

```sh
lxcited help destroy
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

### Use lxcited along with `sudo`

For some reasons, when the `lxcited` executable is located in you ``~/bin`` or in some other custom path, ``sudo`` can't reach it and you can't run:

```sh
sudo lxcited
```

If you want to be able to run lxcited with ``sudo``, instead of installing it in a custom path, you can copy or symlink your file in ``/usr/local/bin`` or any other "well-known path" that will fit the ``sudo`` command.

## License

This piece of software is published under the terms of the WTFPL

See: http://www.wtfpl.net/ for more details, but here is its core term:

   0. You just DO WHAT THE FUCK YOU WANT TO.
