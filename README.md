A Shell Scripting Framework
===========================

This framework is currently a couple of tools written to help manage
scripts and functions in dash/bash on a GNU/Linux (Debian/Ubuntu)
system.

Install
-------

This is not really designed for "installation" yet. It's only really
three scripts so they can simple be copied into the relevant
directories or symlinked into the relevant directories; both methods
work.

UI Scripts
----------

### Script: `ssf`

`ssf` currently has two commands: `fun` and `new`, they aren't
particularly consistent at the moment but I'll fix that.

  - `fun` fetches the function definition from the specified filename.
    It's a wrapper for `print_function` described below.
  - `new` creates a new script in the `~/.scripts` folder (default).
    It is a wrapper for `new_script` described below.

Utility Scripts
---------------

### Script: `new_script`

Creates a Bash script named after the argument.

  - Checks that the script doesn't already exist, exits if so.
  - Creates the script in the same folder as `new_script`
  - Makes the script executable by the user
  - Opens the script pre-populated with a hashbang ready for editing.

#### Dependencies

  - The `EDITOR` environment variable must be set.

### Script: `print_function`

Prints the contents of a function to STDOUT.

  - Checks the specified function exists in `$FUNCPATH`
  - Uses `cat` and `sed` to print the function to `STDOUT` with an
    "infoline".

#### Dependencies

  - The `FUNCPATH` environment variable must be set.

#### Issues

  - Retains blank lines
