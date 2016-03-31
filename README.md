# `pa`: ergonomic `pacman` wrapper for MSYS2

`pa` is a tiny wrapper for `pacman`
that improves on a few of `pacman`'s lousy ergonomics.

`pa` is not strictly MSYS2-only,
but it is developed to be used specifically in MSYS2.

## Usage

`pa` has four commands, each mapping directly to some invocation of `pacman`:

* `install <package>` to install `<package>`
* `remove <package>` to remove `<package>`
* `search <pattern>` to search for `<pattern>` in a `pacman` mirror
* `upgrade` to upgrade either the core system or all userland packages

`pa` has a simple completion of its own
and additionally delegates to the official `pacman` completion, if available.

## Installation

Clone the repository and copy or link the files:

```sh
cp pa /usr/bin/ && cp _pa /usr/share/bash-completion/completions/pa
```

## Motivation

As far as package managers go, `pacman` is technically quite strong.
Unfortunately its UI was not made for mere mortals
and induces considerable mental and physical friction.
The Arch Linux community has written a number of `pacman` wrappers already,
but to my knowledge they all prioritise integrations (e.g. AUR) over ergonomics.

I don't use Arch Linux so I don't use `pacman` much either,
nor do I care about extra integrations.
I do use MSYS2, however, and that uses `pacman` (successfully).
I cope by hiding `pacman` behind a humane UI abstraction layer.

`pa`'s commands are chosen to be 

* **intuitive:** they shall have optimal semantic encoding
* **unambiguous:** they shall have optimal cued recall
* **ergonomic:** they shall be easy to both type out and complete
