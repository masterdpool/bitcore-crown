bitcore-crown
=============

This package is under development. It may be unstable, or not work as expected.

Prerequisites
=============

Currently, it can be only run on Ubuntu.

You need to have ZeroMQ and tools, nvm, Node.js and npm installed.

ZeroMQ and Tools
----------------

```bash
sudo apt-get install libzmq3-dev build-essential
```

Also make sure Python 2.x is installed.

nvm, Node.js and npm
--------------------

Install [nvm](https://github.com/creationix/nvm).

Use `nvm` command to install Node.js v4 and the latest npm:

```bash
nvm install 4
nvm install-latest-npm
```

Installation
============

```bash
npm install -g bitcore-crown
```

Note: Do not use `sudo`. To get rid of `sudo`, Node.js and npm must be installed via `nvm`.

Usage
=====

```bash
bitcored-crown
```

It will start a Crown node and Insight service. The blockchain data will be downloaded to `~/.bitcore-crown`. Insight can be visited via "http://localhost:3001/insight/".

Don't modify `~/.bitcore-crown/bitcore-node-crown.json`. Unlike the original Bitcore, modifying this file will have no effect. This is to avoid conflicts between the testing environment and production environment. In the future this may be changed.

If you think the data is broken, the last way is to delete `~/.bitcore-crown` and start the program to redownload the data.

There's another command `bitcore-crown-adv` for advanced operations. This maps to the `bitcore` command in the original Bitcore. The original Bitcore manual is [here](https://bitcore.io/). We added the `-adv` suffix to avoid confusion with `bitcored-crown`.

Contributing
============

See `CONTRIBUTING.md` file.

License
=======

See `LICENSE` file.
