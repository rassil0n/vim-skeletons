=============
VIM Skeletons
=============

This tiny VIM Skeletons plugin allows you to define a skeleton file per file
type, which is used whenever you create a new file of that type.

Installation
------------

For installation I recommend using vim-plug, a package manager for VIM plugins.
If you have vim-plug running, the following line in your
``.vimrc``/``.config/init.vim`` enables the plugin

```vim
Plug "rassil0n/vim-skeletons"
```

Now you run

```vim
    :PlugInstall
```

and you're done.

If you prefer any other VIM plugin manager, you will find your way according to
your preferences. If you do not use a VIM plugin manager, you should use one.

I ship an example skeleton for your pleasure. Take a look in the ``skeletons/``
directory. Note, that this skeleton will not be used by Skeletons by default.

Usage
-----

Using Skeletons is easy. Just install the plugin and put your skeleton files
into

```
    ~/.config/nvim/extra/skeletons/
```

a skeleton file name must follow the simple format ``whatever.<ft>`` where
``<ft>`` is the file type you want to register the skeleton for. If you have
mutliple files for one type, Skeletons will simply use one. Which one? No idea.
Therefore I recommend to use ``skeleton.<ft>`` by convention to avoid this
issue.

If you want to change the directory where skeletons are stored, take a look at
`Configuration`_.

Configuration
-------------

You can influence the bahavior of Skeletons by two confiuguration variables:

``g:skeletons_dir``

Set this variable to a different directory if you don't want to have your
skeletons to be located in ``~/.config/nvim/extra/skeletons/``.

``g:skeletons_autoregister``

Set this to ``0`` in order to avoid Skeletons to auto-register its
autocommand for inserting the skeletons. You need to do this action
yourself then.
