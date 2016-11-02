---
layout: post
category : nil
tags : []
---

Notes to myself as I go through [Closure for the Brave and True](http://www.braveclojure.com/using-emacs-with-clojure/).

Setup
-----

I was using Emacs app on OS X. Problems with path when running Lein from Emacs.

This fixed it: http://stackoverflow.com/questions/13243048/mac-osx-emacs-24-2-and-nrepl-el-not-working?lq=1

Using Ctrl with the up and down arrows in the REPL is clashing with OS X wanting to show all running apps. There is an answer in the comments. `M-n, M-p` also clashing with one of my own bindings. `C-c C-n, C-c C-p` may be useful.

In section 4, the buffer containing the stace trace isn't appearing from nrepl or when compiling current buffer. It does come up for errors when evaluating expressions in the code buffer though.
