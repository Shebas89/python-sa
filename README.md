pgbackup
========

CLI for backup remote PostgresSQL database either locally or S3.

Preparing the Development
-------------------------

1. Ensure ``pip`` and ``pipenv`` are installed.
2. Clone repository: ``git clone git@github.com:shebas89/pgbackup``
3. ``cd`` into the repository.
4. Fetch development dependencies ``make install``
5. Activate virtualenv: ``pipenv shell``

Usage
-----

Pass in a full database URL, the storage driver, and the destination

S3 Example w/ bucket name:

::

    $ pgbackup postgres://bob@explamble.om:5432/db_one --driver s3 backups

Local example w/ local path:

::

    $ pgbackup postgres://bob@explamble.om:5432/db_one --driver local/var/local/db-one/backup/dump.sql

Running Tests
-------------

Run tests locally using make ``make`` if virtualenv is activated:

::

    $ make

if virtualenv is not activated:

::

    $ pipenv run make
    
