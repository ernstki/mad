
# mad(1)

  `mad(1)` is a markdown driven manual page viewer,
  this makes manuals easier to _write_, _reuse_, and
  _read_.

## Usage

    Usage: mad <file>

    Options:

      -U, --update-self  update mad(1) itself
      -u, --update       update remote mad-pages
      -v, --version      output mad version
      -h, --help         output this help information
      -l, --list         list mad-pages
      -                  read from stdin

## Installation

  Install `mad(1)` and its associated mad page.

    $ make install

  Uninstall both `mad(1)` and the associated mad page.

    $ make uninstall

  Install/update `mad-pages`, a distribution of useful mad
  pages:

    $ mad --update

  These will, by default, be installed to the directory
  `$HOME/.local/share/mad`.

## Page lookup

  Use the __MAD_PATH__ environment variable to control
  where `mad(1)` will look for a manual page.
  The ".md" extension may be omitted.

  For example:
  
    MAD_PATH="$HOME/mad"

  The following paths will **always** be searched, after any
  __MAD_PATH__ defined in the environment:
  
     - .
     - $HOME/.local/share/mad
     - /usr/local/share/mad
     - /usr/share/mad

## Configuration

  For its formatting rules, `mad(1)` installs and sources
  `../etc/mad.conf` relative to `mad`'s installation
  location (_e.g._, `$HOME/.local/etc/mad.conf`)

  You may edit this file directly, or if you're scared of
  overwriting it when updating `mad(1)` you can copy this
  file to something like `~/.mad.conf` and `export
  MAD_CONFIG=~/.mad.conf`.

```
heading: 1m
code: 90m
strong: 1m
em: 4m
```

## Source code

  <https://github.com/ernstki/mad>

## Author

  [TJ Holowaychuk](https://github.com/tj)

