.. _unbilledchargesummary:

UnbilledChargeSummary
=====================
Charge view summary

::

  type UnbilledChargeSummary {
  
    count: Long

    sum: BigDecimal

    issuePeriodEnd: Long
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
