# binaries
> Store built configuration for CI testing

The `main.tar` is bundled confiugration file from [jcs-emacs]().

We attempted to use filename `{{ matrix.os }}.{{ matrix.emacs-version }}.tar`;
but it will instantly kills our 1G of LFS quota. Hence we have only one built
file from each platforms and Emacs versions.
