.. _allinvoiceitemcursor:

AllInvoiceItemCursor
====================
AllInvoiceItemCursor

::

  type AllInvoiceItemCursor {
    
    count: Int
    
    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [ItemSpecification] 
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
