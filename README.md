## What is? | [Download](https://github.com/sudo-give-me-coffee/strace-file/releases/download/continuous/strace-file)
**strace-file** is a wrapper for **strace** that list all files accessed by application with a friendly output

## Usage
```
usage: strace-file [option] PROG [ARGS]

Options:
  -n  Only non existing
  -e  Only existing files (default behaviour)
  -a  Both nonexistent and existing files
  -s  Only files in /usr, /lib, /lib64, /var, /bin and /sbin
  -b  Exclude /usr/share, /usr/local/share and /var
  -v  Prints version of strace-file

Notes for in Flatpak usage, is needed to pass as first parameter:
  ¹ --allow=devel to flatpak will add SYS_PTRACE capability
  ² --appimage-extract-and-run to strace-file
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
