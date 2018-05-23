.. _ticket:

Ticket
======
Tickets (work orders)

::

  type Ticket {
  
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

    creationTime_iso: String

    creationTime: Milliseconds

    closedTime_iso: String

    closedTime: Milliseconds

    heldUntil_iso: String

    heldUntil: Milliseconds

    seconds: Int

    summary: String

    statusText: String

    unread: Boolean

    description: String

    ticketUuid: UUID

    # Arguments
    # filter: [Not documented]
    Account(filter: [AccountFilter]): Account

    # Arguments
    # filter: [Not documented]
    AssignedOperator(filter: [SubscriptionFilter]): Subscription
  }

Required by
-----------
:ref:`allticketcursor`
  *AllTicketCursor*
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`ticketcursor`
  *null*
