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

## Remove a package

1. Remove the submodule entry from `.gitmodules` file
2. Remove the submodule entry from `.git/config`
3. Run `git rm --cached packages/<package-name>`
4. Remove the submodule directory: `rm -rf packages/<package-name>`
5. Remove the submodule directory from `.git/modules/`: `rm -rf .git/modules/packages/<package-name>`
6. Commit the changes: `git commit -m "Remove <package-name> submodule"`


## Update submodules
1. Run `git submodule update --remote --merge`
2. Commit the changes: `git commit -am "Update submodules"`
3. Push the changes: `git push origin main`
4. If you have made changes to the submodules, make sure to push those changes to their respective repositories as well.

## Remove Local Submodules
1. Run `git submodule deinit -f -- packages/<package-name>`