.. _allplancursor:

AllPlanCursor
=============
AllPlanCursor

::

  type AllPlanCursor {

    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Plan]
  }

Required by
------------
:ref:`query`
  *Smile's GraphQL Query type*
