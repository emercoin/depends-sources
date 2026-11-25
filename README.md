# Emercoin Core depends sources

Mirror of the third-party source archives used by the `depends/` build system of
[Emercoin Core](https://github.com/emercoin/emercoin).

The archives are stored as assets of the [`sources`](https://github.com/emercoin/depends-sources/releases/tag/sources)
release, under the file names used in `depends/packages/*.mk`:

    https://github.com/emercoin/depends-sources/releases/download/sources/<file name>

`depends/` tries this mirror first, then the upstream download location and the Bitcoin Core
mirror. Every archive is checked against the SHA256 hash in its package recipe, wherever it
was downloaded from, so the mirror cannot change what gets built.

The files are the unmodified upstream releases, each under its own license.

To add the archives for a new package version, run `contrib/devtools/depends-mirror.sh`
in the Emercoin Core source tree.
