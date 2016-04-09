# Sensible Bash

An attempt at saner Bash defaults. Inspired by Tim Pope's [sensible.vim](https://github.com/tpope/vim-sensible).

## The config

Sensible Bash is intended to be a simple starting point for a better Bash user experience out of the box.

Refer to the commented [source](https://github.com/mrzool/bash-sensible/blob/master/sensible.bash) for a complete list of all the options with explanations. Here's a taste:

#### Smarter tab completion

Readline bindings to improve on Bash's default tab completion:

- Perform file completion in a case insensitive fashion
- Treat hyphens and underscores as equivalent
- Display matches for ambiguous patterns at the first press of the tab key (instead of requiring two tab-presses)

#### Saner history defaults

Sensible defaults for the command history:

- Append to the history file instead of overwriting it
- Save multi-line commands as one command
- Record each line as it gets issued
- Keep track of a bigger history
- Avoid duplicate entries
- Avoid recording unneeded commands (`exit`, `ls`, `bg`, `fg`, and `history` itself)
- Use a [standard ISO 8601](https://tools.ietf.org/html/rfc3339) timestamp for recording commands (ex: `2016-04-09 13:06:31`)

Read more about the settings used here in the article [Better Bash History](http://blog.sanctum.geek.nz/better-bash-history/) by Tom Ryder.

#### Faster file system navigation

Options that considerably speed up the ability to navigate throughout the file system:

- Prepend `cd` to directory names automatically, so you can change to a directory just by typing its name
- Automatically correct spelling errors during tab-completion and in arguments supplied to `cd`
- Set more targets to the `cd` command besides the current working directory (ex: `projects`, `repos`, `documents`, etc)
- Define paths as variables and `cd` into it from anywhere, kind of like a bookmarking system for Bash (`cdable_vars`)

## Usage

You can copy `sensible.bash` in your `bashrc`, cherry-pick the options you like, or source the file at the top of your `bashrc`:

```bash
if [ -f ~/bin/sensible.bash ]; then
   source ~/bin/sensible.bash
fi
```

### Caveats

In order to get Sensible Bash to work correctly, make sure that:

- You're running at least Bash 4.x (`echo $BASH_VERSION`). OS X users: Read [this](https://johndjameson.com/blog/updating-your-shell-with-homebrew/) to install and set up Bash correctly.
- You have the [Bash Completion](http://bash-completion.alioth.debian.org/) package installed and properly configured on your system. ([instructions for OS X](http://davidalger.com/development/bash-completion-on-os-x-with-brew/))
- If you're on OS X, I recommend to follow [Josh Staiger's advice](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html) and source `bashrc` from `bash_profile` so to keep all your configuration in one place.

## Contributing

Consider this as a work in progress where everything is open for discussion. **I'm looking for feedback!** Feel free to open an issue, submit a pull request, or let me know on [Twitter](https://twitter.com/mrzool_) if you think I've missed something important. Same goes for options you think should be removed.

## See also

- My [article](http://mrzool.cc/writing/sensible-bash/) about Sensible Bash
- My [dotfiles](https://github.com/mrzool/dotfiles) for more \*nix configuration goodies
- [Unix as IDE](https://github.com/mrzool/unix-as-ide), my ebook port of the excellent [post series](http://blog.sanctum.geek.nz/series/unix-as-ide/) by Tom Ryder

## License

[MIT](https://opensource.org/licenses/MIT)
