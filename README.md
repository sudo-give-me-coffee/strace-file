## What is?
**strace-file** is a wrapper for **strace** that list all files accessed by application with a friendly output

## Usage
```
usage: strace-file [option] PROG [ARGS]

Options:
  -n    Prints only non existing files
  -a    Prints both nonexistent and existing files
  -e    Prints only existing files (default behaviour)
  -v    Prints version of strace-file
```

## Sample output:

```
$ ./strace-file bash --version
/bin/bash
/etc/ld.so.cache
/lib/x86_64-linux-gnu/libtinfo.so.5
/lib/x86_64-linux-gnu/libdl.so.2
/lib/x86_64-linux-gnu/libc.so.6
/dev/tty
/usr/lib/locale/locale-archive
/usr/share/locale/locale.alias
/usr/share/locale-langpack/pt_BR/LC_MESSAGES/bash.mo
/usr/lib/x86_64-linux-gnu/gconv/gconv-modules.cache
/usr/share/locale-langpack/pt/LC_MESSAGES/bash.mo

```
