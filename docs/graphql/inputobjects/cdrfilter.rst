.. _cdrfilter:

CdrFilter
=========

::

  input CdrFilter {
  
    tid: Int

    ucdrUuid: UUID

    cdrUuid: UUID

    version: Int

    modified: Milliseconds

    subscriptionUuid: UUID

    stid: Long

    bindingUuid: UUID

    aggregateUuid: UUID

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
 }


Required by
------------
:ref:`subscription`
  *A subscription to a service*
:ref:`ucdr`
  *Unmediated CDR*
