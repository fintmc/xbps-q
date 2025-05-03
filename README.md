# xbps-q: QOL wrapper for xbps-query

[`xbps`](https://github.com/void-linux/xbps) is the Void Linux
binary package manager. It's good because it's simple but it is
lacking some features I would wish it had, so I made this script.

## Usage

```console
$ xbps-q --help
xbps-q: better wrapper for xbps-query
Usage: xbps-q [flags...] <matches...>
       xbps-q [flags...] -T <package>
Options:
   -h (--help)               Display a help message
   -P (--flag) <FLAG>        Pass a flag FLAG to xbps-query
   -R (--regex, --regexp)    Search by regexp
   -i                        Ignore case when searching
   -N (--only-names,         Display only names of packages
       --short)
   -T (--this)               Display info for a single specific package
                              (conflicts with some options)
  --installed                Display only installed packages
                              (conflicts with --not-installed)
  --not-installed            Display only not installed packages
                              (conflicts with --installed)
```

## Examples:

Find packages including `git` in the name or description:
```console
$ xbps-q git
```

Find packages that are installed that include `bash` in the name or description:
```console
$ xbps-q bash --installed
```

Print minimal information about the package `git`:
```console
$ xbps-q -T git --short
```

## Building

This is just a bash script, you don't need to build it.

## Installing

Just put the script somewhere in one of the PATH directories.
