![GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)

# ssass-mode
This mode is a clean-room clone of Natalie Weizenbaum's [sass-mode](https://github.com/nex3/sass-mode),
with a few compromises to support mmm-mode. If sass-mode doesn't break for you,
use that.

## Features
- Syntax highlighting
- Syntactic indentation
- `mmm-mode` support

## Limitations
Because parsing Sass with regular expressions is difficult, a few concessions
were made with syntax highlighting. ssass-mode differs from sass-mode in the
following ways

- Class selectors must start with a letter to be highlighted
- ID selectors must start with a lowercase letter to be highlighted

To prevent false-positives with lowercase hex colors, I recommend the excellent
[rainbow-mode](http://git.savannah.gnu.org/cgit/emacs/elpa.git/tree/packages/rainbow-mode)
for color highlighting.

## Installation
ssass-mode should be on MELPA soon, but for now, `(load-file "ssass-mode.el")`
in your `.emacs.d/init.el` should be used for installation.

## Functions
- `ssass-mode` - Enable ssass mode
- `ssass-eval-buffer` - Run the current buffer through Sass, and display the output
- `ssass-eval-region` - Run the current region through Sass, and display the output

## Default Keybindings

- `C-c C-r` - `sass-eval-region`
- `C-c C-c` - `sass-eval-buffer`

## License
GPLv3+
