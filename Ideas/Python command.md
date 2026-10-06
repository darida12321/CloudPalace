The `python` command generally looks like this:
`python [-bBdEhiIOPqRsSuvVWx?] [-c cmd | -m module-name | script | - ] [args]`

Arguments are parsed by [[Python sys module|sys module]] as `sys.argv[0]` and so on.

Its main modes of operation are:
- **`-c command`**: Execute python statements given(`python -c "print 'hi'"`).
- **`-m module-name`**: [[Python module|Module]] is loaded using the [[Python import system|import system]], and executed as a script.
- **`-`**: Read commands from standard input.
- **`<script>`**: Execute code in **file** or **directory** with `__main__.py`.

### Options
Some of these also have an associated environment variable. 

**Generic options:**
- `-?`, `-h`, `--help`: Print all command line options and environment variables.
- `--help-env`: Print environment variables.
- `--help-xoptions`: The `-X` option is left to be implementation specific.
- `--help-all`: Print complete usage information.
- `-v`, `--version`: Print version number.
- `-q`: Don't display copyright and version messages.

**Miscellaneous options:**
- `-b`: Issue a warning when converting [[Python bytes|bytes]] or [[Python bytearray|bytearray]] to [[Python string|str]] without encoding.
- `-bb`: Same as `-b`, but issue an error.

- `-B`: Python won't try writing `.pyc` files (such as in `__pycache__`).
- `--check-hash-based-pycs`: Set how python handles outdated `.pyc` files.

- `-d`: Turn on parser debugging output.
- `-i`: After the script execute, don't close. Keep an interactive shell open.
- `-u`: Force stdout and stderr to be unbuffered.
- `-v`: Print a message when a [[Python module|module]] is initialized.
- `-vv`: Print a message for each file that was searched for a module.
- `-W arg`: Warning control. `-Walways` means warn every time. Lots of options. 

- `-E`: Ignore `PYTHON*` environment variables.
- `-P`: Don't add potentially unsafe path to `sys.path` (current dir, script's dir, etc).
- `-s`: Don't add user [[Python site module|site]] packages to `sys.path`.
- `-S`: Disable the import of the [[Python site module|site]] module.
- `-I`: Isolated mode. Combination of `-E`, `-P` and `-s`, plus potentially more restrictions.

- `-O`: Remove [[Python assert statement|assert]] statements, and [[Python if statement|conditionals]] with `__debug__`.
- `-OO`: Do `-O`, but also remove **docstrings**.

- `-R`: Turn on hash randomization.
- `-x`: Skip first line of source, allowing non-Unix `#!cmd` headers.

- `-X`: Reserved for implementation-specific things


