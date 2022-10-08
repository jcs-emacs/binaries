<a href="#"><img src="https://raw.githubusercontent.com/jcs-emacs/badges/161a8e892ac7a9e90cc8add538e49025ebb66b71/others/built-with/dark.svg" alt="Built with"></a>
<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/jcs-emacs/jcs-elpa/master/docs/etc/logo/light/sink.png">
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/jcs-emacs/jcs-elpa/master/docs/etc/logo/dark/sink.png">
  <img width="25%" align="right" src="">
</picture>

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
