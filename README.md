# ivy-clipmenu.el

[Ivy](https://github.com/abo-abo/swiper#ivy) integration with the clipboard manager, [clipmenu](https://github.com/cdown/clipmenu).

Usually `clipmenu` integrates with `rofi` or `dmenu`. This Emacs module
integrates with `ivy`. Launch this when you want to select a clip.

## Dependencies
- `ivy.el`
- `clipmenu`

## Installation

To use this module, you must first install `clipmenu` and ensure that the
`clipmenud` daemon is running. Refer to the [installation
instructions](https://github.com/cdown/clipmenu#installation)
for those details.

Also ensure that you have the `ivy` module available in your Emacs. Consult the
[installation instructions](https://github.com/abo-abo/swiper#installation) for
more information.

`ivy-clipmenu` is available on [MELPA](https://github.com/melpa/melpa). To
install you may need to run:

- `M-x` `package-refresh-contents`
- `M-x` `package-install` `ivy-clipmenu`

## Configuration

This module intentionally does not define any keybindings since I'd prefer
not to presume my users' preferences. Personally, I use
[EXWM](https://github.com/ch11ng/exwm)
as my window manager, so I call `exwm-input-set-key` and map it to
`ivy-clipmenu/copy`. Your setup may look something like this:

```elisp
(require 'ivy-clipmenu)
(global-set-key (kbd "C-M-v") #'ivy-clipmenu/copy)
```

Clipmenu itself supports a variety of environment variables that allow you to
customize its behavior. These variables are respected herein. If you'd
prefer to customize clipmenu's behavior from within Emacs, refer to the
variables defined in this module.

For more information:
- See `clipmenu --help`.
- Visit github.com/cdown/clipmenu.
