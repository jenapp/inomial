.. _tarifftypefilter:

TariffTypeFilter
================

::

  input TariffTypeFilter {
  
    tid: Int

    tariffType: Long

    rateType: String

    path: [Long]

    name: String

    tariffTypeUuid: UUID
  }

Required by
------------
:ref:`cdr`
  *Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.*
