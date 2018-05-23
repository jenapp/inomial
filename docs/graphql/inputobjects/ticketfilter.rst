.. _ticketfilter:

TicketFilter
============

::

  input TicketFilter {
  
    ticket: Int

    number: String

    ticketType: Int

    ticketTypeName: String

    ticketPriority: Int

    ticketPriorityName: String

    ticketStatus: Int

    ticketStatusName: String

    ticketGroup: Int

    account: Int

    targetSubscription: Int

    targetTx: Int

    submittingSubscription: Int

    assignedOperator: Int

    creationTime: Milliseconds

    closedTime: Milliseconds

    heldUntil: Milliseconds

    seconds: Int

    summary: String

    statusText: String

    unread: Boolean

    description: String

    ticketUuid: UUID
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
:ref:`query`
  *Smile's GraphQL Query type*
