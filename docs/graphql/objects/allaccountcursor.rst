.. _allaccountcursor:

AllAccountCursor
================
AllAccountCursor

::

  type AllAccountCursor {
  
    count: Int
    
    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Account]
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
