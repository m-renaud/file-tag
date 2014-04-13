# File-Tag

File-tag is a utility for adding tags to files.

## Dependencies

- pip (https://pypi.python.org/pypi/pip or in your distros package manager)
- sh  (`pip install sh`)

## Installation

- Add the `ft` and `update-ft` executables to your `$PATH`.
- Run `update-ft` to create the database (this will eventually do a rescan to take into account any changed file locations).

## Usage

There are four main options for `ft`:

- `find (<query> | --all)`
  + Find all files with the given tags, or all files if no tags are given.
  + Intersection is the default operator between terms.
  + Union can be specified with "or".
  + Difference is accomplished with a minus sign before the tag.
  + *Example:* `ft find a b or c d -e`

- `add <filename> <tags>`
  + Add all tags to filename
  + *Example:* `ft add foo.cxx ref cxx boost spirit`

- `rm <filename> (<tags> | --all)`
  + Removes all tags from filename.
  + *Example:* `ft rm foo.cxx spirit`

- `list <filename>...`
  + Lists all tags for all filenames given.
  + *Example:* `ft list *`

