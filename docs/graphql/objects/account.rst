.. _account:

Account
=======
A debtor record containing transactions.

::

  type Account {
  
    account: Long

    accountUuid: UUID

    usn: String

    alternateAccountNumber: String

    accountType: Int

    accountTerms: Int

    accountDisposition: Int

    discount: Int

    creationTime_iso: String

    creationTime: Milliseconds

    accountCostCentre: Int

    description: String

    taxable: Boolean

    taxSchedule: Int

    currency: String

    timezone: Int

    uoobject: Int

    custom: String

    # Arguments
    # filter: [Not documented]
    Subscriptions(filter: [SubscriptionFilter]): SubscriptionCursor

    # Arguments
    # filter: [Not documented]
    Txs(filter: [TxFilter]): [Tx]

    # Arguments
    # filter: [Not documented]
    Contact(filter: [AccountContactFilter]): [AccountContact]

    # Arguments
    # filter: [Not documented]
    Address(filter: [AccountAddressFilter]): [AccountAddress]

    # Arguments
    # filter: [Not documented]
    CostCentre(filter: [AccountCostCentreFilter]): AccountCostCentre

    # Arguments
    # filter: [Not documented]
    Tickets(filter: [TicketFilter]): TicketCursor

    # Arguments
    # filter: [Not documented]
    Bindings(filter: [BindingFilter]): BindingCursor

    # Arguments
    # filter: [Not documented]
    PaymentMethods(filter: [PaymentMethodFilter]): [PaymentMethod]
  }

Required by
-----------
:ref:`allaccountcursor`
  *AllAccountCursor*
:ref:`draftinvoice`
  *Draft invoice*
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`searchresult`
  *A single result from a search query*
:ref:`subscription`
  *A subscription to a service*
:ref:`ticket`
  *Tickets (work orders)*
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
:ref:`txdetail`
  *Detailed information about a (possibly draft) transaction*
