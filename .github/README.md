# scripts

Here are all the scripts I use. I store these in a `.scripts` folder in my `$HOME` directory.

## documentation

Remember to run `chmod +x *` in the newly cloned repository, and export your `$PATH` to include this directory.
```
export PATH="$PATH:$HOME/.scripts"
```

* `compiler` -- renders/compiles source code opened in `vim` based on file extension when executed. 

	* currently supports the following file extensions: `.rmd` (R-Markdown), `.tex` (LaTeX), `.md` (Markdown), `.c` (C source code), `.py` (Python source code), `.scm` (Scheme source code).

	* to run, put the following lines in your `.vimrc`, open any compatible source code, and press \<leader\>-C (usually \\-c):
	```
	set shellcmdflag=-ic
	map <leader>c :!compiler <c-r>%<CR>
	```

* `replace_space` -- replaces all spaces within filenames with underscores in the current directory.
	
	* this doesn't work for folders, and is not recursive. i hope to extend this someday into a larger script that can replace filenames with any regex.

* `setwallpaper` -- script that sets a colorscheme based on a random image in a specified folder using `wal` and then uses `feh` to set the wallpaper.

	* set your wallpaper folder accordingly by defining `$bgdir`.

* `lock` -- just a bunch of command flags delimitted by newlines for i3lock-color.
	
	* the lockscreen image must be named `i3lockscreen` in your `.scripts` folder.

## license

* all scripts in this repository are licensed under the MIT License as free and open source software. see `LICENSE` for more details.
