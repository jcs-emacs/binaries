# binaries
> Store built configuration for CI testing

The `main.tar` is bundled confiugration file from [jcs-emacs]().

We attempted to use filename `{{ matrix.os }}.{{ matrix.emacs-version }}.tar`;
but it will instantly kills our 1G of LFS quota. Hence we have only one built
file from each platforms and Emacs versions.

## 📂 Handle Git LFS

Before we explode our large file storge (LFS), our strategy here is to revert
anything to our very first main `.tar` file's commit using the
`git reset --hard <commit_id>` command. Then we force push `git push --force`
our tar file to this repository, in order to make our LFS' disk space **low**.

Commit SHA: `c128b3c19c16c3f95d126359546e0bca32274eb9`
