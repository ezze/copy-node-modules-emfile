# copy-node-modules-emfile

This repo reproduces [copy-node-modules](https://github.com/arloliu/copy-node-modules) error looking like this:

`Error: EMFILE: too many open files, open '/var/data/store/nfsshare/soft/copy-node-modules-emfile/node_modules/spdx-exceptions/README.md',Error: EMFILE: too many open files, open '/var/data/store/nfsshare/soft/copy-node-modules-emfile/dist/node_modules/spdx-exceptions/README.md',Error: EMFILE: too many open files, open '/var/data/store/nfsshare/soft/copy-node-modules-emfile/node_modules/spdx-exceptions/index.json'`

While everything works on Ubuntu 16.04 LTS the error occurs on CentOS 7.

[Here is a relevant StackOverflow question](https://stackoverflow.com/q/8965606/506695).

## How to reproduce

1. Clone the repo:

```
$ git clone git@github.com:ezze/copy-node-modules-emfile
```

2. Install dependencies:

```
$ yarn
```

3. Run copy script:

```
$ yarn copy
```
