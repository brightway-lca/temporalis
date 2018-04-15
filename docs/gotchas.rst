Gotchas
=======

Set database to `static` for faster calculations
------------------------------------------------

If you are using a database that does not contain any temporal information (e.g ecoinvent) you'd better set its attribute `static` to `True` after registering the database with Brigthway2. By doing so during the graph traversal the datasets encountered from such a databases are solved with the traditional matrix-based approach. Despite not mandatory this will sensibly improve your calculation time giving same results.

After having `created <https://chris.mutel.org/inventory-models.html>`_ or `imported <https://docs.brightwaylca.org/notebooks.html#importing-data-example-notebooks>`_ your database in Brigthway2, just :

.. code-block:: python

    databases['<my_db_name>']['static']=True
    databases.flush()
    
If you later on modify the database adding temporal information you should change it to:

.. code-block:: python

    databases['<my_db_name>']['static']=False
    databases.flush()
    
to avoid the temporal informations are incorrectly skipped. By default when you registering the database in Brigthway2 it is traverersed by the graph traversal.
