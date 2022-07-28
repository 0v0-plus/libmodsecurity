# libmodsecurity

## Introduction

This repo provides an unofficial build based on [SpiderLabs/ModSecurity](https://github.com/SpiderLabs/ModSecurity).

`GitHub Actions` automatically check the latest release and build the library.

We follow the official compilation guide on `Ubuntu` and use the following command.

```shell
./configure --prefix=/usr/local/modsecurity
make -j$(nproc)
make install
```

## Usage

Download from release and extract to `/usr/local` . Files may be organized like this

```text
/
└── usr
    └── local
        ├── modsecurity
        │   ├── bin
        │   │   └── ... # something
        │   ├── include
        │   │   └── ... # something
        │   └── lib
        │       └── ... # something
        ├── other
        └── other
```

Then edit `/etc/profile` , append `export LIB_MODSECURITY=/usr/local/modsecurity` at the end.

Finally, execute `source /etc/profile` .
