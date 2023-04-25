# notes-waves
text files with ideas, explanations etc (very informal for now)

- why is there cog-extract-recursive and cog-delete-recursive ?
cog-delete-recursive: does remove atom from storage (aka RocksDB)
cog-extract-recursive: does NOT remove atom from storage (aka RocksDB)

Example:
- if you have a ListLink with several ConceptNodes (say: "D","E","F") and call `(cog-extract-recursive! (Concept "F"))`, then "F" disappears as well as the list.

### guile + gdb
I had to use the source package for gdb, since the standard package didn't enable guile support.
The following had to be executed:
`./configure --with-guile`
