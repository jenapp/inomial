.. _cdr:

Cdr
====
Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.


::

  type Cdr {
  
    tid: Int

    ucdrUuid: UUID

    cdrUuid: UUID

    version: Int

    modified_iso: String

    modified: Milliseconds

    subscriptionUuid: UUID

    stid: Long

    bindingUuid: UUID

    aggregateUuid: UUID

    effective_iso: String

    effective: Milliseconds

    duration: Long

    cdrType: String

    src: Long

    dst: Long

    tariffCode: String

    quantity: Long

    cost: BigDecimal

    tariffType: Long

    chargeAmount: BigDecimal

    # Arguments
    # filter: [Not documented]
    Subscription(filter: [SubscriptionFilter]): Subscription

    # Arguments
    # filter: [Not documented]
    Errors(filter: [CdrErrorFilter]): [CdrError]

    # Arguments
    # filter: [Not documented]
    TariffType(filter: [TariffTypeFilter]): TariffType
  }

Required by
-----------
:ref:`cdrcursor`
  *null*
:ref:`ucdr`
  *Unmediated CDR*
