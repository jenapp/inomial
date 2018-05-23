.. _cdrerror:

CdrError
=========
CDR processing errors. These are deleted once a CDR has been successfully processed.

::

  type CdrError {
  
    error: Long

    logTime_iso: String

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
-------------
:ref:`cdr`
  *Charge Data Record (CDR). In Smile, a CDR is a record of a single element of a billable event.*
