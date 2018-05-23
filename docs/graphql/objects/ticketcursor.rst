.. _ticketcursor:

TicketCursor
============

::

  type TicketCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Ticket]
  }
  
Required by
-------------
:ref:`account`
  *A debtor record containing transactions*
