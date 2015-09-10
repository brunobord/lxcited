# Contributing to lxcited

Contributions are very welcome. Here's how you can help.

## If you've got a bug, an issue, an idea

* Check if this issue is not already opened, or this idea not already [in the issue list](https://github.com/brunobord/lxcited/issues) before opening it.
* Describe your problem as precisely as you can, mention which version of ``lxcited`` you're using.


## I want to make a pull-request

Here's a tiny checklist you'll have to take into account when pushing a pull-request forward.


### If you're adding a new command

- [ ] Add the command in the ``lxcited.autocomplete``, both in the first opts variable and in the autocomplete bit to distinguish between "running-only", "stopped-only", "container-neutral" or "no-container" commands.
- [ ] Add the help text.
- [ ] *Optional*: add the extra help text.
- [ ] Check that this help text is correctly formatted, by typing ``lxcited help``, ``lxcited help <new command>``.

### If you're modifying the behaviour of a command

- [ ] Check that its help text is still OK.
- [ ] Eventually modify the help text to make it relevant.

### Final checks

- [ ] Check that the autocomplete for your new or edited command is still working and didn't break other autocompletes.
- [ ] If you're solving an existing issue, don't forget to make a #(issue num) reference in your commit(s) and / or in your PR description.
- [ ] Amend the ``CHANGELOG.md`` file, using the appropriate subsection.

Please ping me if you see that this pull-request has not been commented or reviewed, I may have missed it.
