Known Issues
============

BW2Package incompatibility
--------------------------

For now it is not possible to `export <https://docs.brightwaylca.org/technical/bw2io.html#bw2io.package.BW2Package.export_obj>`_ a database containing :ref:`temporal` with `bw2io <https://docs.brightwaylca.org/technical/bw2io.html>`_ 

For example:

.. code-block:: python

    from bw2io.package import BW2Package

    export_db = Database('example')
    filename = 'temporalis_test'
    filepath = r"path\to\folder"

    export = BW2Package.export_obj(export_db, filename, filepath)


Returns the error:

.. code-block:: python

    TypeError: Object of type 'TemporalDistribution' is not JSON serializable
    
