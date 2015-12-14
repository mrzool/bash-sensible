# sensible.bash

An attempt at saner Bash defaults. Inspired by Tim Pope's [sensible.vim](https://github.com/tpope/vim-sensible).

**Work in progress!**

## Usage

Download `sensible.bash` and source it at the top of your `bashrc` like this:

```bash
if [ -f ~/bin/sensible.bash ]; then
   source ~/bin/sensible.bash
fi
```

If you're on OS X, I recommend you to follow [Josh Staiger's advice](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html) of sourcing `bashrc` from `bash_profile` so to keep all your configuration in one place.

## Customization

A couple of things in `sensible.bash` are intended to be customized:

- **`CDPATH`** to define where cd will look for target beside your current working directory
- **`cdable_vars`**, variables containing paths that allow you to jump in your favorite places across the file system at the speed of thought

Refer to the comments in `sensible.bash` and [to my article](http://mrzool.cc/writing/sensible-bash/) for the details.


## Further resources

- [The art of command line](https://github.com/jlevy/the-art-of-command-line)
- [Command-line one liners](http://arturoherrero.com/command-line-one-liners/)
- [Bioinformatics one liners](https://github.com/stephenturner/oneliners)
- [What is your single most favorite command-line trick using Bash?](http://stackoverflow.com/questions/68372/what-is-your-single-most-favorite-command-line-trick-using-bash) on Stack Overflow

## License

[MIT](https://opensource.org/licenses/MIT)
