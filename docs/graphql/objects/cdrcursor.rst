.. _cdrcursor:

CdrCursor
===========


::

  type CdrCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Cdr]
  }

Required by
-----------
:ref:`subscription`
  *A subscription to a service*
