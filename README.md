Tools for Shell Scripting
=========================

This is a couple of tools written to help manage scripts and
functions in dash/bash on a GNU/Linux (Debian/Ubuntu) system.

Utility Scripts
---------------

### `new_script`

Creates a Bash script named after the argument.

  - Checks that the script doesn't already exist, exits if so.
  - Creates the script in the same folder as `new_script`
  - Makes the script executable by the user
  - Opens the script pre-populated with a hashbang ready for editing.

	new_script my_script

#### Dependencies

The `EDITOR` environment variable should be set.
