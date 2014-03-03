ShLibs
======

This is a collection of libraries to some bash sweetness in POSIX sh.

Usage is like importing in C : 

::

    # Include arrays
    . shlibs_array

    # Include hash
    . shlibs_hash

    # ... your code ...

They will export some functions in your current Shell. Note that the
implementation is done in a pure shell idiom, ie with lots of temporary files.
It should not be an issue, but it's best to be aware of it. 

Everything is located into a temporary directory created with ``mktemp -d``. It
should therefore honors the environment variables.
