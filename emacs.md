# Using Emacs

### Dealing with indentation in shared files

The general view in Emacs world is that [tabs are evil](http://emacswiki.org/emacs/TabsAreEvil) and that [the ASCII #9 TAB character should never appear in disk files](http://www.jwz.org/doc/tabs-vs-spaces.html), but if I am sharing my code with non-Emacs users, most of whom are using tabs to indent their code, this is not something that I can easily enforce.

The way to deal with this is pretty simple. Add:

    (setq default-tab-width 2)

to the `.emacs` file.

This ensures that tabs are indented by just two spaces and also (for reasons I do not fully understand) that the tabs are preserved in any added code (at least in `html-mode`). If in doubt, I can run `M-x tabify` before saving and committing a file.
