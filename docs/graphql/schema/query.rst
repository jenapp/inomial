.. _query:

Query
=====
Smile's GraphQL Query type

::

  type Query {
    
    # Returns the account for the given UID.
    #
    # Arguments
    # uid: [Not documented]
    # uuid: [Not documented]
    # usn: [Not documented]
    account(uid: Int, uuid: UUID, usn: String): Account
    
    # Returns the subscription for the given UID.
    #
    # Arguments
    # uid: [Not documented]
    # uuid: [Not documented]
    # usn: [Not documented]
    subscription(uid: Int, uuid: UUID, usn: String): Subscription
    
    # Returns (possibly draft) transaction details.
    #
    # Arguments
    # uuid: [Not documented]
    # number: [Not documented]
    txDetail(uuid: UUID, number: String): TxDetail
    
    # Returns transaction.
    #
    # Arguments
    # uuid: [Not documented]
    # number: [Not documented]
    # tx: [Not documented]
    tx(uuid: UUID, number: String, tx: String): Tx
   
    # Performs the equivalent of a UI search
    #
    # Arguments
    # q: The query string
    # limit: The number of results to return, up to 200
    search(q: String, limit: Int): [SearchResult]
    
    # Returns UCDRs.
    #
    # Arguments
    # uuid: [Not documented]
    ucdr(uuid: UUID): Ucdr
    
    # Returns the ticket for the given ID.
    #
    # Arguments
    # id: [Not documented]
    # uuid: [Not documented]
    # number: [Not documented]
    ticket(id: Int, uuid: UUID, number: String): Ticket
    
    # Returns the draft invoice for the given ID.
    #
    # Arguments
    # uuid: [Not documented]
    # number: [Not documented]
    draftInvoice(uuid: UUID, number: String): DraftInvoice
    
    # Returns all unbilled charge summary.
    unbilledChargeSummary: [UnbilledChargeSummary]
    
    # Returns all draft invoices.
    #
    # Arguments
    # filter: [Not documented]
    allDraftInvoices(filter: [DraftInvoiceFilter]): AllDraftInvoiceCursor
   
    # Returns all tickets.
    #
    # Arguments
    # filter: [Not documented]
    allTickets(filter: [TicketFilter]): AllTicketCursor
    
    # Returns all accounts.
    #
    # Arguments
    # filter: [Not documented]
    allAccounts(filter: [AccountFilter]): AllAccountCursor
    
    # Returns all subscriptions.
    #
    # Arguments
    # filter: [Not documented]
    allSubscriptions(filter: [SubscriptionFilter]): AllSubscriptionCursor
    
    # Returns all plans.
    #
    # Arguments
    # filter: [Not documented]
    allPlans(filter: [PlanFilter]): AllPlanCursor
    
    # Returns all invoice items.
    #
    # Arguments
    # filter: [Not documented]
    allInvoiceItems(filter: [ItemSpecificationFilter]): AllInvoiceItemCursor
  }


Required by
-----------
This element is not required
