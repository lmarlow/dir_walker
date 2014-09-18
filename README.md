DirWalker
=========

DirWalker lazily traverses one or more directory trees, depth first, 
returning successive file names.

Initialize the walker using

    {:ok, walker} = DirWalker.start_link(path) # or [path, path...]

Then return the next `n` path names using

    paths = DirWalker.next(walker [, n \\ 1])

Successive calls to `next` will return successive file names, until
all file names have been returned. 