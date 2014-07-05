Tox User Install
================

Install Toxic and its dependencies as user.

Description
-----------

I wanted to use `toxic` on Debian but it is not currently packaged so I had
to compile it. I didn't want to `make install` as root since I don't think
this is a clean solution, so I made this script to automate the installation
with shared libraries in my home.

Installation
------------

Example installation in `~/opt` directory.

```sh
mkdir -p ~/opt
cd "$_"
git clone https://github.com/valeriangalliat/tox-user-install.git
tox-user-install/tox-user-install
```

This will create `~/opt/tox`, containing `libsodium`, `toxcore` and `toxic`,
and a `usr` directory containing the C headers and shared libraries.

You'llhave to define the `LD_LIBRARY_PATH` environment variable to contain
`~/opt/tox/usr/local/lib` to be able to launch `toxic`.