Release History
===============

.. :changelog:

v0.3b5 (2017-11-26) : I Need a Miracle
---------------------------------------

New
~~~
- Mishmash_cmd session-scoped fixture.
- Library 'excludes' option. Fixes #202.
- orm length limit constants
- More ORM limit tests, truncation, validation.
- Use mishmash.util.safeDbUrl for displayed/logged password obfuscation.
- Add Track.metadata_format and Track.METADATA_FORMATS.

Changes
~~~~~~~
- Moved VARIOUS_TYPE detection info _albumTypeHint.
  less noise about lp->various conversion
- Close DB connections after commands.
- Better logging for debugging VARIOUS_TYPE coersion.
- Moved limit constants to each ORM class.
- Docker updates.

Fix
~~~
- PServeCommand requires .ini extension.
- Show used config files.
- Some (not all) truncation for colomn limits and \x00 handling.
- Make docker-publish.
- Dup config section error.


v0.3b4 (2017-05-14) : Triumph Of Death
-----------------------------------------

New
~~~
- Init(scope=False), for wrapped SessionMaker with
  sqlalchemy.orm.scoped_session.
- Mishmash.web is optional, and packaged as extra [web] install.
- Mishmash.VARIOUS_ARTISTS_NAME == gettext("Various Artists")

Changes
~~~~~~~
- Removed various artist config and started gettext.

Fix
~~~
- Mishmash.web working again.

Other
~~~~~
- Update eyed3 from 0.8.0b1 to 0.8 (#108) <github-bot@pyup.io>
- Pin pyramid to latest version 1.8.3 (#94) <github-bot@pyup.io>


v0.3b3 (2017-04-09) : Prayers for Rain
---------------------------------------

New
~~~
- UTC sync times and per lib last_sync. Fixes #6, #7.
- Db test fixtures, etc.

Changes
~~~~~~~
- mishmash.data.init now returns the 3-tuple (engine, SessionMaker, connection).
  Previously a 2-tuple, sans connection, was returned.
  The new mishmash.database.DatebaseInfo namedtuple is the actual return type,
  if you prefer not to unpack the return value.

v0.3b2 (2017-03-12) : Nine Patriotic Hymns For Children
-------------------------------------------------------

Fix
~~~
- Protect against not being the first to call
  multiprocessing.set_start_method.


v0.3b1 (2017-03-12) : Nine Patriotic Hymns For Children
-------------------------------------------------------

New
~~~
- Mismash sync --monitor (using inotify)
- Test beginnings.

Changes
~~~~~~~
- Label_id renamed tag_id. Fixes #65.
- Mishmash.database.init accepts the DB URL as its first arguments, NO
  LONGER a Config object.

Fix
~~~
- Postgres service on Travis-CI.
- Restored gitchangelog fork.


v0.3b0 (2017-02-26)
-------------------------

* Initial release
