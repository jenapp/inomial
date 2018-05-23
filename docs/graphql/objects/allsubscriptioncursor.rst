.. _allsubscriptioncursor:

AllSubscriptionCursor
=====================
AllSubscriptionCursor

::

  type AllSubscriptionCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Subscription]
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
