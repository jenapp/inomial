.. _alldraftinvoicecursor:

AllDraftInvoiceCursor
====================
AllDraftInvoiceCursor

::

  type AllDraftInvoiceCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [DraftInvoice]
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
