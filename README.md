[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
<a href="https://jcs-emacs.github.io/"><img src="https://raw.githubusercontent.com/jcs-emacs/badges/master/others/built-with/dark.svg" alt="Built with"></a>

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/jcs-emacs/jcs-elpa/master/docs/etc/logo/light/sink.png">
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/jcs-emacs/jcs-elpa/master/docs/etc/logo/dark/sink.png">
  <img width="20%" align="right" src="">
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

## ⚜️ License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [`LICENSE`](./LICENSE) for details.
