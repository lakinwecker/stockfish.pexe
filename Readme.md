stockfish.pexe
==============

A multi-threaded [Stockfish](https://github.com/official-stockfish/Stockfish)
that runs in Chrome using [PNaCl](https://www.chromium.org/nativeclient/pnacl).
Also see [stockfish.js](https://github.com/niklasf/stockfish.js) as a fallback.

Usage
----

See ``nacl/index.html`` for an example.
About 500 KB uncompressed, 400 KB gzipped.

Building
--------

1. Install the NaCl SDK and setup an environment variable
   ``NACL_SDK_ROOT=path/to/nacl_sdk/pepper_49``
2. ``cd nacl``
3. ``make``

Changes to original Stockfish
-----------------------------

* Replace ``src/main.cpp`` with ``src/nacl.cpp``.
* Turn ``UCI::loop`` into ``UCI::command``.
* Remove Syzygy tablebases.

Acknowledgements
----------------

Thanks to [@exoticorn](https://github.com/exoticorn/stockfish-nacl) for
providing a PNaCl module for the older Stockfish 5.
