# scripts

Here are all the scripts I use. I store these in a `.scripts` folder in my
`$HOME` directory.

## documentation

Remember to run `chmod +x *` in the newly cloned repository, and export your
`$PATH` to include this directory.

```
export PATH="$PATH:$HOME/.scripts"
```

* `compile` -- renders/compiles source code based on file extension. just press
  `<Enter>` to compile each time, and keep this in a separate window underneath
  your text editor.

	* currently supports the following file extensions: `.rmd` (R-Markdown),
	  `.tex` (LaTeX), `.md` (Markdown), `.c` (C source code), `.py` (Python
	  script), `.scm` (Scheme source code), `.r` (R script).

	* this can also be run in `vim` for convenience. put the following lines
	  in your `.vimrc`, open any compatible source code, and press
	  `<leader>-C` (the `<leader>` key is usually `\`):

	```
	set shellcmdflag=-ic
	map <leader>c :!compiler <c-r>%<CR>
	```

* `syu` -- my update script. currently, all it does is update a mirror list
  (default `~/.config/pacman.d/mirrorlist`), and then update arch linux.
  remember to update `/etc/pacman.d/mirrorlist` to use the mirror list updated
  by `syu`.

	* wishlist: pull all git repos from remote/origin and update AUR and R
	  packages too.

* `replace_space` -- replaces all spaces within filenames with underscores in
  the current directory.

	* this doesn't work for folders, and is not recursive. i hope to extend
	  this someday into a larger script that can replace filenames with any
	  regex.

* `setwallpaper` -- script that sets a color scheme based on a random image in
  a specified folder using `wal` and then uses `feh` to set the wallpaper.

	* set your wallpaper folder accordingly by defining `$bgdir`.

* `bbg [COMMAND]` -- **b**anish to **b**ack**g**round. uses `nohup` to ignore HUP
  signals upon exit, and directs all STDERR and STDOUT to `/dev/null`.

* `termopen [COMMAND]` -- opens the command in the user's preferred terminal
  specified by the `$TERM` environmental variable.

* `lock` -- just a bunch of command flags delimited by newlines for
  i3lock-color.

	* the lockscreen image must be named `i3lockscreen` in your `.scripts`
	  folder.

## license

* all scripts in this repository are licensed under the MIT License as free and
  open source software. see `LICENSE` for more details.
