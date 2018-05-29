.. _cdrerrorfilter:

CdrErrorFilter
==============

::

  input CdrErrorFilter {
  
    error: Long

    logTime: Milliseconds

    tid: Int

    ucdrUuid: UUID

    cdrUuid: UUID

    errorSource: String

    errorType: String

    errorLevel: String

    args: [String]
  }

Required by
------------
:ref:`cdr`
  *Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.*
