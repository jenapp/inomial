.. _subscriptionfilter:

SubscriptionFilter
==================

::

  input SubscriptionFilter {
  
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

    created: Milliseconds

    accountCostCentre: Int

    description: String

    taxable: Boolean

    currency: String

    timezone: Int

    provisioned: Milliseconds

    activated: Milliseconds

    ordered: Milliseconds

    enabled: Milliseconds

    uoobject: Int

    subscriptionStatus: String

    purchaseOrder: UUID

    custom: String
  }

Required by
------------
:ref:`account`
  *A debtor record containing transactions*
:ref:`cdr`
  *Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.*
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`ticket`
  *Tickets (work orders)*
:ref:`txitem`
  *Transaction line item*
