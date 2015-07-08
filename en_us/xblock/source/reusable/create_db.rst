**************************
Create the SQLite Database
**************************

Before running the XBlock SDK the first time, you must create the SQLite
database.

In the ``xblock_development`` directory, run the following command to create
the database.

   .. code-block:: bash

      (venv) $ python xblock-sdk/manage.py syncdb
