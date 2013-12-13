A Shell Scripting Framework
===========================

This framework is currently a couple of tools written to help manage
scripts and functions in dash/bash on a GNU/Linux (Debian/Ubuntu)
system.

Utility Scripts
---------------

### Script: `new_script`

Creates a Bash script named after the argument.

  - Checks that the script doesn't already exist, exits if so.
  - Creates the script in the same folder as `new_script`
  - Makes the script executable by the user
  - Opens the script pre-populated with a hashbang ready for editing.


	new_script my_script

#### Dependencies

  - The `EDITOR` environment variable must be set.

### Script: `print_function`

Prints the contents of a function to STDOUT.

  - Checks the specified function exists in $FUNCPATH
  - Uses `cat` and `sed` to print the function to STDOUT with an
    "infoline".

#### Dependencies

  - The `FUNCPATH` environment variable must be set.

#### Issues

  - Retains blank lines
