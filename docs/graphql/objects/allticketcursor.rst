.. _allticketcursor:

AllTicketCursor
================
AllTicketCursor

::

  type AllTicketCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Ticket]
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
