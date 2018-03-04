Gotchas
=======

Processes with specific temporal distributions could be incorrectly excluded
----------------------------------------------------------------------------

The initial graph traversal could exclude some nodes which have important temporal dynamics, but whose total demanded amount was small. For example, the following exchange would be excluded as having no impact, because the total amount was zero:

.. code-block:: python

    {
        "amount": 0,
        "temporal distribution": 
        TemporalDistribution(np.array([ 0,  10],dtype='timedelta64[Y]') ,np.array([1.0, -1.0])),  
    }

The best way around this software feature/bug is to create two separate sub-processes, one with the positive amounts and the other with the negative.

.. code-block:: python

    {
        "amount": 1,
        "temporal distribution": 
        TemporalDistribution(np.array([ 0 ],dtype='timedelta64[Y]') ,np.array([1.0])),  
    }

    {
        "amount": -1,
        "temporal distribution": 
        TemporalDistribution(np.array([10],dtype='timedelta64[Y]') ,np.array([-1.0])),  
    }
