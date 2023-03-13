# Stacked Development

Repository that combines all other stacked repositories to ease
the (local) development process. There are no tests/branch
protections in place.

## Installation

1. Clone this repository
2. Run `git submodule update --init`

## Add new package

1. Add the package as a submodule with
   `git submodule add <git-url> packages/<package-name>`
