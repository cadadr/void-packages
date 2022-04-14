# Göktuğ’s XBPS source package collection

This is my fork of the [void-packages] repository, containing my
personal, non-upstreamed packages. Consult [the upstream Readme] and
[documentation] for more information, including build instructions.

[void-packages]: https://github.com/void-linux/void-packages/
[the upstream Readme]: ./Readme_upstream.markdown
[documentation]: ./Manual.md

I have started a fresh git repo to save space and truncated [the
mailmap file](./.mailmap) in order not to redirect spam to addressed
found in the [original .mailmap
file](https://github.com/void-linux/void-packages/blob/master/.mailmap).

This fork starts from [commit 511ffe6].

[commit 511ffe6]: https://github.com/void-linux/void-packages/commit/511ffe6071009c1e6c9a3463c1b1f7a327189e4c

## Basic build instructions

    $ ./xbps-src binary-bootstrap
    $ ./xbps-src pkg <package-name>

To install a package, first build it, then use `xi` from `xtools`:

    $ xi <package-name>

After building and installing a package, consider running

    $ git clean -dfx

to remove unused files, as this reduces the size of the tree from
almost 600MB down to roughly 5.5MB, i.e. by two orders of magnitude.

## Packages found here

- [pomodorino](./srcpkgs/pomodorino): [my simple systray-based
  pomodoro timer](https://gkayaalp.com/pomodorino.html)
