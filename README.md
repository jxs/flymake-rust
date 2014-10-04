flymake-rust.el
==========================

An Emacs flymake handler for syntax-checking Rust source code
using `cargo` or `rustc`.

Installation
=============

If you choose not to use one of the convenient packages in
[Melpa][melpa] and [Marmalade][marmalade], you'll need to add the
directory containing `flymake-rust.el` to your `load-path`, and then
`(require 'flymake-rust)`. You'll also need to install
[flymake-easy](https://github.com/purcell/flymake-easy).

Usage
=====

Add the following to your emacs init file:

    (require 'flymake-rust)
    (add-hook 'rust-mode-hook 'flymake-rust-load)

Checker uses `cargo` by-default. If you want to use `rustc` compiler,
you must add following strings:

    (setq flymake-rust-use-cargo nil)
    (require 'flymake-rust)
    (add-hook 'rust-mode-hook 'flymake-rust-load)


[marmalade]: http://marmalade-repo.org
[melpa]: http://melpa.milkbox.net

<hr>

Thanks [Steve Purcell](https://github.com/purcell) for the help
