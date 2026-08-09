The **site** module is usually automatically imported (unless a `-S` is specified). It handles the updating of `sys.path` with site-packages, where external [[Python package|packages]] might be located.

For example, adds `/usr/lib/python3.14/site-packages` to `sys.path`.
This is important, as [[Python virtual environment|virtual environments]] work by creating their own "site-packages" dir.

**Functions**:
- `getsitepackages()`: Site-packages installed system-wide.
- `getusersitepackages()`: Site-packages installed for the user.






