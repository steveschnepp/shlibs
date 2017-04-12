ShLibs
======

This is a collection of libraries to some bash sweetness in POSIX sh.

.. image:: https://travis-ci.org/steveschnepp/shlibs.svg?branch=master
    :target: https://travis-ci.org/steveschnepp/shlibs

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

shlibs_array
------------

The functions are::

        array_check()
        array_create()
        array_destroy()
        array_len()
        array_push()
        array_pop()
        array_idx()
        array_values()

shlibs_hash
-----------

The functions are::

        hash_check()
        hash_create()
        hash_destroy()
        hash_len()
        hash_set()
        hash_get()
