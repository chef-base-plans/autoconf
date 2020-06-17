[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.autoconf?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# autoconf

## Maintainers

* The Habitat Maintainers: <humans@habitat.sh>

## Type of Package

Binary package

## Usage

The following executables are included with this package:

* autoupdate
* autoheader
* autoscan
* autoconf
* ifnames
* autom4te
* autoreconf

Usage is as follows:

```bash
$ hab pkg install core/autoconf --binlink
$ autoupdate --help
Usage: /bin/autoupdate [OPTION]... [TEMPLATE-FILE]...

Update each TEMPLATE-FILE if given, or `configure.ac' if present,
or else `configure.in', to the syntax of the current version of
Autoconf.  The original files are backed up.

Operation modes:
  -h, --help                 print this help, then exit
  -V, --version              print version number, then exit
  -v, --verbose              verbosely report processing
  -d, --debug                don't remove temporary files
  -f, --force                consider all files obsolete

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ autoheader --help
Usage: /bin/autoheader [OPTION]... [TEMPLATE-FILE]

Create a template file of C `#define' statements for `configure' to
use.  To this end, scan TEMPLATE-FILE, or `configure.ac' if present,
or else `configure.in'.

  -h, --help               print this help, then exit
  -V, --version            print version number, then exit
  -v, --verbose            verbosely report processing
  -d, --debug              don't remove temporary files
  -f, --force              consider all files obsolete
  -W, --warnings=CATEGORY  report the warnings falling in CATEGORY

Warning categories include:
  `cross'         cross compilation issues
  `gnu'           GNU coding standards (default in gnu and gnits modes)
  `obsolete'      obsolete features or constructions
  `override'      user redefinitions of Automake rules or variables
  `portability'   portability issues (default in gnu and gnits modes)
  `syntax'        dubious syntactic constructs (default)
  `unsupported'   unsupported or incomplete features (default)
  `all'           all the warnings
  `no-CATEGORY'   turn off warnings in CATEGORY
  `none'          turn off all the warnings
  `error'         treat warnings as errors

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ autoscan --help
Unescaped left brace in regex is passed through in regex; marked by <-- HERE in m/\${ <-- HERE [^\}]*}/ at /bin/autoscan line 361.
Usage: /bin/autoscan [OPTION]... [SRCDIR]

Examine source files in the directory tree rooted at SRCDIR, or the
current directory if none is given.  Search the source files for
common portability problems, check for incompleteness of
`configure.ac', and create a file `configure.scan' which is a
preliminary `configure.ac' for that package.

  -h, --help          print this help, then exit
  -V, --version       print version number, then exit
  -v, --verbose       verbosely report processing
  -d, --debug         don't remove temporary files

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ autoconf --help
Usage: /bin/autoconf [OPTION]... [TEMPLATE-FILE]

Generate a configuration script from a TEMPLATE-FILE if given, or
`configure.ac' if present, or else `configure.in'.  Output is sent
to the standard output if TEMPLATE-FILE is given, else into
`configure'.

Operation modes:
  -h, --help                print this help, then exit
  -V, --version             print version number, then exit
  -v, --verbose             verbosely report processing
  -d, --debug               don't remove temporary files
  -f, --force               consider all files obsolete
  -o, --output=FILE         save output in FILE (stdout is the default)
  -W, --warnings=CATEGORY   report the warnings falling in CATEGORY [syntax]

Warning categories include:
  `cross'         cross compilation issues
  `obsolete'      obsolete constructs
  `syntax'        dubious syntactic constructs
  `all'           all the warnings
  `no-CATEGORY'   turn off the warnings on CATEGORY
  `none'          turn off all the warnings
  `error'         warnings are error

The environment variables `M4' and `WARNINGS' are honored.

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

Tracing:
  -t, --trace=MACRO[:FORMAT]  report the list of calls to MACRO
  -i, --initialization        also trace Autoconf's initialization process

In tracing mode, no configuration script is created.  FORMAT defaults
to `$f:$l:$n:$%'; see `autom4te --help' for information about FORMAT.

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ ifnames --help
Usage: /bin/ifnames [OPTION]... [FILE]...

Scan all of the C source FILES (or the standard input, if none are
given) and write to the standard output a sorted list of all the
identifiers that appear in those files in `#if', `#elif', `#ifdef', or
`#ifndef' directives.  Print each identifier on a line, followed by a
space-separated list of the files in which that identifier occurs.

  -h, --help      print this help, then exit
  -V, --version   print version number, then exit

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ autom4te --help
Usage: /bin/autom4te [OPTION]... [FILES]

Run GNU M4 on the FILES, avoiding useless runs.  Output the traces if tracing,
the frozen file if freezing, otherwise the expansion of the FILES.

If some of the FILES are named `FILE.m4f' they are considered to be M4
frozen files of all the previous files (which are therefore not loaded).
If `FILE.m4f' is not found, then `FILE.m4' will be used, together with
all the previous files.

Some files may be optional, i.e., will only be processed if found in the
include path, but then must end in `.m4?';  the question mark is not part of
the actual file name.

Operation modes:
  -h, --help               print this help, then exit
  -V, --version            print version number, then exit
  -v, --verbose            verbosely report processing
  -d, --debug              don't remove temporary files
  -o, --output=FILE        save output in FILE (defaults to `-', stdout)
  -f, --force              don't rely on cached values
  -W, --warnings=CATEGORY  report the warnings falling in CATEGORY
  -l, --language=LANG      specify the set of M4 macros to use
  -C, --cache=DIRECTORY    preserve results for future runs in DIRECTORY
      --no-cache           disable the cache
  -m, --mode=OCTAL         change the non trace output file mode (0666)
  -M, --melt               don't use M4 frozen files

Languages include:
  `Autoconf'   create Autoconf configure scripts
  `Autotest'   create Autotest test suites
  `M4sh'       create M4sh shell scripts
  `M4sugar'    create M4sugar output

Warning categories include:
  `cross'         cross compilation issues
  `gnu'           GNU coding standards (default in gnu and gnits modes)
  `obsolete'      obsolete features or constructions
  `override'      user redefinitions of Automake rules or variables
  `portability'   portability issues (default in gnu and gnits modes)
  `syntax'        dubious syntactic constructs (default)
  `unsupported'   unsupported or incomplete features (default)
  `all'           all the warnings
  `no-CATEGORY'   turn off warnings in CATEGORY
  `none'          turn off all the warnings
  `error'         treat warnings as errors

The environment variables `M4' and `WARNINGS' are honored.

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

Tracing:
  -t, --trace=MACRO[:FORMAT]  report the MACRO invocations
  -p, --preselect=MACRO       prepare to trace MACRO in a future run

Freezing:
  -F, --freeze   produce an M4 frozen state file for FILES

FORMAT defaults to `$f:$l:$n:$%', and can use the following escapes:
  $$     literal $
  $f     file where macro was called
  $l     line where macro was called
  $d     nesting depth of macro call
  $n     name of the macro
  $NUM   argument NUM, unquoted and with newlines
  $SEP@  all arguments, with newlines, quoted, and separated by SEP
  $SEP*  all arguments, with newlines, unquoted, and separated by SEP
  $SEP%  all arguments, without newlines, unquoted, and separated by SEP
SEP can be empty for the default (comma for @ and *, colon for %),
a single character for that character, or {STRING} to use a string.

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ autoreconf --help
Usage: /bin/autoreconf [OPTION]... [DIRECTORY]...

Run `autoconf' (and `autoheader', `aclocal', `automake', `autopoint'
(formerly `gettextize'), and `libtoolize' where appropriate)
repeatedly to remake the GNU Build System files in specified
DIRECTORIES and their subdirectories (defaulting to `.').

By default, it only remakes those files that are older than their
sources.  If you install new versions of the GNU Build System,
you can make `autoreconf' remake all of the files by giving it the
`--force' option.

Operation modes:
  -h, --help               print this help, then exit
  -V, --version            print version number, then exit
  -v, --verbose            verbosely report processing
  -d, --debug              don't remove temporary files
  -f, --force              consider all files obsolete
  -i, --install            copy missing auxiliary files
      --no-recursive       don't rebuild sub-packages
  -s, --symlink            with -i, install symbolic links instead of copies
  -m, --make               when applicable, re-run ./configure && make
  -W, --warnings=CATEGORY  report the warnings falling in CATEGORY [syntax]

Warning categories include:
  `cross'         cross compilation issues
  `gnu'           GNU coding standards (default in gnu and gnits modes)
  `obsolete'      obsolete features or constructions
  `override'      user redefinitions of Automake rules or variables
  `portability'   portability issues (default in gnu and gnits modes)
  `syntax'        dubious syntactic constructs (default)
  `unsupported'   unsupported or incomplete features (default)
  `all'           all the warnings
  `no-CATEGORY'   turn off warnings in CATEGORY
  `none'          turn off all the warnings
  `error'         treat warnings as errors

The environment variable `WARNINGS' is honored.  Some subtools might
support other warning types, using `all' is encouraged.

Library directories:
  -B, --prepend-include=DIR  prepend directory DIR to search path
  -I, --include=DIR          append directory DIR to search path

The environment variables AUTOM4TE, AUTOCONF, AUTOHEADER, AUTOMAKE,
ACLOCAL, AUTOPOINT, LIBTOOLIZE, M4, and MAKE are honored.

Report bugs to <bug-autoconf@gnu.org>.
GNU Autoconf home page: <http://www.gnu.org/software/autoconf/>.
General help using GNU software: <http://www.gnu.org/gethelp/>.
$ 
```
