build-dependencies
==================

Simple platform-independent build dependency specification.

Supported Platforms
-------------------

- Debian (i.e. [apt-get](https://wiki.debian.org/Apt))
- Darwin (i.e. [homebrew](http://brew.sh/))

Usage
-----

```bash
source dependencies.sh

dep_install source-dir
```

Dependencies are specified in simple text files in specified source directory:

```
# Linux
libcppunit-dev
cmake:1
lcov:1
pkg-config:1
clang:0
```

The line format is:

- Anything starting with `#` is ignored.
- `package name` [ `colon` `mandatory flag`]

The flag specifies if the package is mandatory (1 or omitted entirely) or optional (0).

Requirements
------------

- [GNU Bash](https://www.gnu.org/software/bash/)
- a complete set of command line tools such as `sed`, `grep`, etc.
- `sudo` access

Disclaimer
----------

This script is largely written to build [meta](https://github.com/jfinkhaeuser/meta)
on Travis CI. It might not work well elsewhere.

License
-------

See [LICENSE](./LICENSE).

Authors
-------

See [Authors](./AUTHORS.md).
