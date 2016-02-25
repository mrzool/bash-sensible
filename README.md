# sensible.bash

An attempt at saner Bash defaults. Inspired by Tim Pope's [sensible.vim](https://github.com/tpope/vim-sensible).

## The config

`sensible.bash` is intended to be a simple starting point to enjoy a better Bash experience out of the box. The file has three sections.

### 1. Smarter tab completion

Options to improve on Bash's default tab completion. These settings get Bash to:

1. Perform file completion in a case insensitive fashion;
2. Treat hyphens and underscores as equivalent;
3. Display matches for ambiguous patterns at the first press of the tab key (instead of requiring two tab-presses).

### 2. Sane history defaults

Some tweakings to the command history, mostly taken from Tom Ryder's article [Better Bash History](http://blog.sanctum.geek.nz/better-bash-history/). These options will get Bash to:

1. Append to the history file, instead of overwriting it;
2. Save multi-line commands as one command;
3. Record each line as it gets issued;
4. Keep track of a bigger history;
5. Avoid duplicate entries;
6. Avoid recording unneeded commands (`exit`, `ls`, `bg`, `fg`, and `history` itself);
7. Make use of a timestamp format that is actually useful.

### 3. Better directory navigation

Options to make file system navigation blazingly fast:

1. Prepend cd to directory names automatically, so you can `cd` into directories just by typing their name;
2. Automatically correct spelling errors during tab-completion;
3. Automatically correct spelling errors in arguments supplied to `cd`;
4. `CDPATH` defines where `cd` will look for targets—the default is the current working directory, but you can add directories you want to have fast access to (ex: `projects`, `repos`, `documents`...)
5. `cdable_vars` allows you to define paths as variables and `cd` into it from wherever you are in the file system, kind of like a bookmarking system for Bash.

Refer to the comments in `sensible.bash`  to learn more.

## Usage

You can either copy `sensible.bash` in your `bashrc` or cherry-pick the options you like most from it, but the fastest way to get started is probably to source it from the top of your `bashrc`:

```bash
if [ -f ~/bin/sensible.bash ]; then
   source ~/bin/sensible.bash
fi
```

#### Note for OS X users

If you're using OS X, I recommend to follow Josh Staiger's [advice](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html) and source `bashrc` from `bash_profile` so to keep all your configuration in one place.

## Further resources

- [My article](http://mrzool.cc/writing/sensible-bash/) where I explain each option in detail.
- [The art of command line](https://github.com/jlevy/the-art-of-command-line)
- [Command-line one liners](http://arturoherrero.com/command-line-one-liners/)
- [Bioinformatics one liners](https://github.com/stephenturner/oneliners)
- [What is your single most favorite command-line trick using Bash?](http://stackoverflow.com/questions/68372/what-is-your-single-most-favorite-command-line-trick-using-bash) on Stack Overflow

## License

[MIT](https://opensource.org/licenses/MIT)
