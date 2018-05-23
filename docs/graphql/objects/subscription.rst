.. _subscription:

Subscription
============
A subscription to a service

::

  type Subscription {
  
    subscription: Long

    subscriptionUuid: UUID

    usn: String

    username: String

    account: Int

    masterSubscription: Int

    service: Int

    ratingCycle: String

    ratingCycleDay: Int

    discount: Int

    created_iso: String

    created: Milliseconds

    accountCostCentre: Int

    description: String

    taxable: Boolean

    currency: String

    timezone: Int

    provisioned_iso: String

    provisioned: Milliseconds

    activated_iso: String

    activated: Milliseconds

    ordered_iso: String

    ordered: Milliseconds

    enabled_iso: String

    enabled: Milliseconds

    uoobject: Int

    subscriptionStatus: String

    purchaseOrder: UUID

    custom: String

    # Arguments
    # filter: [Not documented]
    Account(filter: [AccountFilter]): Account

    # Arguments
    # filter: [Not documented]
    CostCentre(filter: [AccountCostCentreFilter]): AccountCostCentre

    # Arguments
    # filter: [Not documented]
    Service(filter: [ServiceFilter]): Service

    # Arguments
    # filter: [Not documented]
    Cdrs(filter: [CdrFilter]): CdrCursor

    # Arguments
    # filter: [Not documented]
    SubscriptionBindings(filter: [SubscriptionBindingFilter]): SubscriptionBindingCursor
  }

Required by
-----------
:ref:`allsubscriptioncursor`
  *AllSubscriptionCursor*
:ref:`cdr`
  *Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.*
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`searchresult`
  *A single result from a search query*
:ref:`subscriptioncursor`
  *null*
:ref:`ticket`
  *Tickets (work orders)*
:ref:`txitem`
  *Transaction line item*
