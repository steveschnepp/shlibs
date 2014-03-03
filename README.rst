ShLibs
======

This is a collection of libraries to some bash sweetness in POSIX sh.

Usage is like importing in C::

    # Include arrays
    . shlibs_array

    # Include hash
    . shlibs_hash

    # ... your code ...

They will export some functions in your current shell process.

Note that the implementation is done in a pure shell idiom, using *lots* of
temporary files.

That should not be a real issue, as everything is located into a temporary
directory created with ``mktemp -d``, so it should therefore honor relevant
environment variables. It should also be quite fast as the file involved are
usually quite small.
