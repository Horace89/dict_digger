dict_digger
===========

Digs into Dicts

Useful syntax for digging into nested dictionaries, and removes the need to check if a key exists, or handling of
KeyError


Installation
------------

.. code-block:: bash

    $ pip install dict_digger


Usage
-----

.. code-block:: python

    import dict_digger

    h = {
        'a': {
             'b': 'tuna',
             'c': 'fish'
         },
         'b': {}
    }

    result = dict_digger.dig(h, 'a','b')
    print result  # prints 'tuna'

    result = dict_digger.dig(h, 'c','a')
    print result # prints None
    # Important!!  Does not through an error, just returns None



Alternatives
------------

.. code-block:: python

    try:
        result = h['c']['a']
    except KeyError:
        bill_to = None

Testing
-------

We are using nose

.. code-block:: bash

    $ nosetests

