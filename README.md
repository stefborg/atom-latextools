# LaTeXTools for Atom

by Marciano Siniscalchi

This is an *in-progress* Atom port of the [LaTeXTools package](http://github.com/SublimeText/LaTeXTools) for Sublime Text (currently maintained by Ian Bacher and myself).

Currently (v0.2.0, 1/4/2016), the following features are implemented:

* Compile and view PDF files (Windows and OSX only for now), using the `MikTeX` distribution and the `SumatraPDF` previewer on Windows, and `MacTeX` and `Skim` on OSX.
* Parse the tex log output and list errors and warnings in the "LaTeXTools console." Jumping to errors is *not yet implemented*, but will be shortly.
* Full support for multi-file projects by adding  `%!TEX root = master.tex` at the top of each included file.
* Virtually all LaTeXTools snippets.

**Keybindings**: by default, these are essentially the same as in Sublime Text, except that the **build** command is bound to `C-alt-b`, where `C` is `ctrl` on Windows and `cmd` on OSX. All other commands are triggered via combinations that start with `C-l`. As in Sublime, the "select line" command is remapped to `C-l,C-l`. 

Missing functionality to be implemented, roughly in the order I plan to add it:

* Jumping to errors and warnings by clicking in the LaTeXTools console.
* Compiling and viewing on OS X (and possibly Linux)
* Reference / citation completion
* Wrapping selection in commands or environments, and similar facilities
* Fill helper (autocompletion of various commands, such as  `\include`/`\input`, `\usepackage`, `\includegraphics`, etc.)
* Toggling functions on/off: e.g., temporarily stop jumping to the current line in the PDF file after compilation.
* Better documentation :)
* Other functionality in the Sublime Text package


The package does **not** provide syntax highlighting. Rather, it is supposed to be used in conjunction with the `language-latex` package: this *must* be installed for snippets to work.

*Warning*: you will see many package settings. For now, only a few are actually honored. You are better off leaving everything as per defaults, except possibly for the path to your tex distro and PDF previewer (if necessary).

A final note: there are a couple of other nice LaTeX packages for Atom. Each implements a specific function: compiling / viewing,  reference completion, etc. However, the objective of this package is to provide the *entire* functionality of the LaTeXTools plugin for Sublime Text, so current users of that editor can comfortably move to Atom.

Help is welcome!