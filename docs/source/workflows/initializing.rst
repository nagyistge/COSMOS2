.. _initializing:

Initializing
===============

Cosmos is initialized using the :class:`cosmos.Cosmos` object, which is subsequently used to start instances of :class:`Workflow`
which contain the entire structure of a workflow.

.. code-block:: python

    from cosmos import Cosmos
    cosmos = Cosmos('sqlite:///my_cosmos_db.sqlite')
    cosmos.initdb()
    workflow = cosmos.start('My_Workflow')

You will likely have to install the python package required to use the driver you'd like. For example, if you are using
``postgres+psycopg2:///``, make sure you ``pip install psycopg2``.  See `SQLAlchemy Engines <http://docs.sqlalchemy.org/en/latest/core/engines.html>`_
for more details.


API
-----------

Cosmos
_______


.. autoclass:: cosmos.api.Cosmos
    :members: __init__, initdb, start, resetdb, runweb

.. autofunction:: cosmos.api.default_get_submit_args
