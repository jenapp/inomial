.. _subscriptioncursor:

SubscriptionCursor
==================

::

  type SubscriptionCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Subscription]
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
