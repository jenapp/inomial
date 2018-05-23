.. _ucdr:

Ucdr
=====
Unmediated CDR

::

  type Ucdr {
  
    tid: Int

    ucdrUuid: UUID

    created_iso: String

    created: Milliseconds

    cdr: String

    source: Int

    # Arguments
    # filter: [Not documented]
    Cdrs(filter: [CdrFilter]): [Cdr]
  }

Required by
------------
:ref:`query`
  *Smile's GraphQL Query type*
