===================
Welcome to MishMash
===================

Music database and web interface.

Status
------
.. image:: https://img.shields.io/pypi/v/MishMash.svg
   :target: https://pypi.python.org/pypi/MishMash/
   :alt: Latest Version
.. image:: https://img.shields.io/pypi/status/MishMash.svg
   :target: https://pypi.python.org/pypi/MishMash/
   :alt: Project Status
.. image:: https://travis-ci.org/nicfit/MishMash.svg?branch=master
   :target: https://travis-ci.org/nicfit/MishMash
   :alt: Build Status
.. image:: https://img.shields.io/pypi/l/MishMash.svg
   :target: https://pypi.python.org/pypi/MishMash/
   :alt: License
.. image:: https://img.shields.io/pypi/pyversions/MishMash.svg
   :target: https://pypi.python.org/pypi/MishMash/
   :alt: Supported Python versions
.. image:: https://coveralls.io/repos/nicfit/MishMash/badge.svg
   :target: https://coveralls.io/r/nicfit/MishMash
   :alt: Coverage Status

Features
--------

* Free software: GNU GPL v3.0 license
* MishMash is a music database using `Python`_ and `SQLAlchemy`_.
* A command-line tool for building and managing a music database.
* Web browser interface (using `Pyramid`_) for browsing your music library.
* Uses `eyeD3`_ for reading MP3s and ID3 metadata.
* Support and tested with Python 3.4 and Postgresql. SQLite is periodically
  tested with, but future features may not be supported (e.g. full text
  search).

.. _Python: https://www.python.org/
.. _SQLAlchemy: http://www.sqlalchemy.org/
.. _eyeD3: http://eyeD3.nicfit.net/
.. _Pyramid: https://trypyramid.com/

Getting Started
----------------
::

    $ mishmash info
    /\/\_____  .__       .__        _____                .__   /\/\
    \(\(     \ |__| _____|  |__    /     \ _____    _____|  |__\(\(
      /  \ /  \|  |/  ___/  |  \  /  \ /  \\__  \  /  ___/  |  \
     /    Y    \  |\___ \|   Y  \/    Y    \/ __ \_\___ \|   Y  \
     \____|__  /__/____  >___|  /\____|__  (____  /____  >___|  /
             \/        \/     \/         \/     \/     \/     \/

    Version              : 0.3
    Database URL         : sqlite:////~/mishmash.db
    Database version     : 0.3
    Last sync            : Never
    Configuration files  : <default>


    === Music library ===
    0 music tracks
    0 music artists
    0 music albums
    0 music tags


Surprise, you now have an empty sqlite database in your home directory.
Let's leave it here for now, it can be located elsewhere or use a different
database using command line arguments and/or environment variables. Pretty
useless, so now add some music.::

    $ mishmash sync /home/travis/Music/Melvins
    Syncing library 'Music': paths=['/home/travis/Music/Melvins/']
    Syncing directory: /home/travis/Music/Melvins/
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    eyed3.mp3.headers:WARNING: Lame tag CRC check failed
    Syncing directory: /home/travis/Music/Melvins/1984 - Mangled Demos
    Adding artist: Melvins
    Syncing directory: /home/travis/Music/Melvins/1986 - 10 Songs
    Adding album: 10 Songs
    Adding track: /mnt/Media/Media/audio/music/Melvins/1986 - 10 Songs/Melvins - 01 - Easy As It Was.mp3
    Updating album: 10 Songs
    ...
    == Library 'Music' sync'd [ 8.73s time (45.9 files/s) ] ==
    401 files sync'd
    401 tracks added
    0 tracks modified
    0 orphaned tracks deleted
    0 orphaned artists deleted
    0 orphaned albums deleted


