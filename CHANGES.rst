Version 0.6.0-RC1
------------------

Unreleased

-   Use ``should_set_cookie`` for preventing each request from saving the session again.
-   Permanent session otherwise empty will not be saved.
-   Use `secrets` module to generate session identifiers, with 256 bits of
    entropy (was previously 122).
-   Explicitly name support for python-memcached, pylibmc and pymemcache.
-   Introduce SESSION_KEY_LENGTH to control the length of the session key in bytes, default is 32.
-   Fix pymongo 4.0 compatibility.
-   Fix expiry is None bug in SQLAlchemy.
-   Fix bug when existing SQLAlchemy db instance.
-   Support SQLAlchemy SESSION_SQLALCHEMY_SEQUENCE, SESSION_SQLALCHEMY_SCHEMA and SESSION_SQLALCHEMY_BINDKEY
-   Drop support for Redis < 2.6.12.
-   Fix empty sessions being saved.
-   Support Flask 3.0 and Werkzeug 3.0

Version 0.5.0
-------------

Released 2023-05-11

-   Drop support for Python < 3.7.
-   Switch to ``pyproject.toml`` and Flit for packaging.
-   Move to Pallets Community Ecosystem for community-driven maintenance.
-   Replace use of ``session_cookie_name`` for Flask 2.3 compatibility.


Version 0.4.1
-------------

-   Temporarily pin Flask < 2.3.


Version 0.4.0
-------------

-   Added support for ``SESSION_COOKIE_SAMESITE``.


Version 0.3.2
-------------

-   Changed ``werkzeug.contrib.cache`` to ``cachelib``.


Version 0.3.1
-------------

-   ``SqlAlchemySessionInterface`` is using ``VARCHAR(255)`` to store session id now.
-   ``SqlAlchemySessionInterface`` won't run `db.create_all` anymore.


Version 0.3
-----------

-   ``SqlAlchemySessionInterface`` is using ``LargeBinary`` type to store data now.
-   Fixed ``MongoDBSessionInterface`` ``delete`` method not found.
-   Fixed ``TypeError`` when getting ``store_id`` using a signer.


Version 0.2.3
-------------

-   Fixed signing failure in Python 3.
-   Fixed ``MongoDBSessionInterface`` failure in Python 3.
-   Fixed ``SqlAlchemySessionInterface`` failure in Python 3.
-   Fixed ``StrictRedis`` support.


Version 0.2.2
-------------

-   Added support for non-permanent session.


Version 0.2.1
-------------

-   Fixed signing failure.


Version 0.2
-----------

-   Added ``SqlAlchemySessionInterface``.
-   Added support for cookie session id signing.
-   Various bugfixes.


Version 0.1.1
-------------

Fixed MongoDB backend ``InvalidDocument`` error.


Version 0.1
-----------

-   First public preview release.
