[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.autoconf?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# autoconf

GNU Autoconf is a tool for producing configure scripts for building, installing and packaging software on computer systems where a Bourne shell is available.  See [documentation](https://www.gnu.org/software/autoconf/)

## Maintainers

* The Core Planners: <chef-core-planners@chef.io>

## Type of Package

Binary package

### Use as Dependency

Binary packages can be set as runtime or build time dependencies. See [Defining your dependencies](https://www.habitat.sh/docs/developing-packages/developing-packages/#sts=Define%20Your%20Dependencies) for more information.

To add core/autoconf as a dependency, you can add one of the following to your plan file.

##### Buildtime Dependency

> pkg_build_deps=(core/autoconf)

##### Runtime dependency

> pkg_deps=(core/autoconf)

### Use as Tool

#### Installation

To install this plan, you should run the following commands to first install, and then link the binaries this plan creates.

``hab pkg install core/autoconf --binlink``

will add the following binaries to the PATH:

* /bin/autoupdate
* /bin/autoheader
* /bin/autoscan
* /bin/autoconf
* /bin/ifnames
* /bin/autom4te
* /bin/autoreconf

#### Using an example binary

You can now use the binary as normal.  For example:

``/bin/autoconf --help`` or ``autoconf --help``

```bash
$ autoconf --help
Usage: /bin/autoconf [OPTION]... [TEMPLATE-FILE]

Generate a configuration script from a TEMPLATE-FILE if given, or
`configure.ac' if present, or else `configure.in'.  Output is sent
to the standard output if TEMPLATE-FILE is given, else into
`configure'.

Operation modes:
...
...
```
